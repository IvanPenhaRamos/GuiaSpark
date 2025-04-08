## Acciones comunes en RDDs:

- .count Devuelve el número de elementos

- .first Devuelve el primer elemento

- .take (n) Devuelve un array (Scala) o una lista (Python) de los primeros n elementos

- .collect Devuelve un array (Scala) o una lista (Python) de todos los elementos

```python
myRDD.count()

myRDD.first()

myRDD.take(2)

myRDD.collect()
```