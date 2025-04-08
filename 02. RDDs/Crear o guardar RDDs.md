# Resilient Distributed Datasets
---

Cear RDDs desde archivos de texto mapeando cada línea como elemento de un array tipo string

```python
RDDdesdeTXT = spark.sparkContext.textFile("archivo.txt")

RDDdesdeData = sc.textFile("pathDeMiData/")

RDDdesdeLogs = spark.sparkContext.textFile("mydata/*.log")

RDDdesdeMásDeUnTXT = spark.sparkContext.textFile("archivo1.txt,archivo2.txt")
```

*sc.wholeTextFiles* mapea cada archivo de un directorio como elemento de un único RDD

>Sólo es útil con archivos pequeños porque lo debe soportar la memoria

```python
userRDD = sc.wholeTextFiles("NombreDirectorio/")
```

**RDDs desde colecciones**

Se usan para testing, generar datos de forma programada, integrar con otras librerías o sistemas o aprendizaje.

```python
myData = ["Alice","Carlos","Frank","Barbara", "Alice"]

myRDD = sc.parallelize(myData)
```


**Salvando RDDs**

Para guardar el RDD como archivo de texto plano

Hay que poner el nombre de un directorio, no de un archivo ya que al ser un archivo distribuido tendrá diferentes nombres.

```python
myRDD.saveAsTextFile("mydata/")
```

