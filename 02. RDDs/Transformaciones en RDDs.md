Ejemplos de transformaciones:

- .distinct Crea un nuevo RDD eliminando los elementos duplicados

- .union(rdd) Crea un nuevo RDD uniendo la data de un RDD en otro

- .map(function) Crea un nuevo RDD ejectuando la función en cada elemento del RDD origen

- .filter(function) Crea un nuevo RDD incluyendo o excluyendo cada registro del RDD en base a una función booleana

- .flatMap

- .mapPartitions

```python
myRDD.distinct().collect()

myRDD.union(RDDdesdeData)

myRDD.map(lambda x: x.upper())

myRDD.filter(lambda x: x.startswith("A"))
```

**Transformaciones entre RDDs**

- .union(RDD) Une **todos** los elementos de los dos RDDs

- .intersection(RDD) Devuelve los elementos que tienen en común ambos RDDs

- .substract(RDD) Elimina los elementos del RDD parametrizado al RDD original

```python
r1 = [1,2,3,3]
r2 = [2,4]

rdd1 = sc.parallelize(r1)
rdd2 = sc.parallelize(r2)

rdd1.union(rdd2).collect()

rdd1.intersection(rdd2).collect()

rdd1.subtract(rdd2).collect()
```