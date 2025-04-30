# 🚀 GUÍA APACHE SPARK

El propósito de esta 📚 **guía de referencia** es crear un lugar de consulta intermedio entre la basta documentación que uno puede encontrar en internet y un simplista *cheatsheet* para trabajar con **Apache Spark** (tanto en **PySpark** como en **Scala**).

📌 Esta guía toma como base el material formativo de *Cloudera Educational Services*, incluyendo ejemplos.

⚠️ *No se cuenta con el consentimiento expreso de la compañía*, por lo que **no debe usarse con fines profesionales** ni para impartir **formación propia**.

🛠️ Actualmente se planea crear versiones tanto para **PySpark** como para **Scala**.

✍️ A lo largo del documento, se usa `DF` como abreviatura de `DataFrame` por economía del lenguaje.

## ÍNDICE 🔎

01.  🧱  **RDDs**

    - Resilient Distributed Datasets

    - Crear RDDs desde archivos de texto

    - Crear RDDs desde colecciones

    - Salvando RDDs

    - Acciones comunes en RDDs

    - Transformaciones

    - Transformaciones entre RDDs

02.  🧮  **DataFrames**

    - Introducción a DataFrames

    - Atributos y métodos 

03.  📥  **DataFrames - Lectura y escritura**

    - Lectura y escritura de DataFrames

    - Formatos soportados por Spark SQL

    - Integración con Pandas

    - Lectura

    - Escritura

04.  🛠️  **DataFrames - Operaciones**

    - Operaciones con DFs

    - Acciones más comunes (`count`, `first`, `take`, `show`, `collect`, `write`)

    - Transformaciones (definición, inmutabilidad de DFs igual que RDDs)

05.  🧩  **DataFrames - Columnas**

    - Las columnas de los DataFrames

    - Métodos, funciones y manejo de columnas

06.  🧬  **DataFrames - Complex Types**

    - Arrays 

    - Maps 

    - Structs 

07.  🔗  **DataFrames - Joins - Combining and splitting**

    - Combining and Splitting DataFrames

    - Joins

    - Tipos de Join

    - Operaciones de conjuntos o sets a los DataFrames

    - Métodos de conjunto: `Union`, `Intersect` y `Subtract`

    - Splitting a DataFrame (.randomSplit, parámetro seed)

08.  📈  **DataFrames - Funciones estadísticas y de agrupación**

    - Summarizing data with aggregate functions

    - Funciones de agregación

    - Grouping data

    - Pivoting data

09.  🧑‍💻 **DataFrames - UDF User Defined Function**

    - Pasos para utilizar UDF

    - Aspectos a tener en cuenta

    - Razones de ineficiencia

    - Cómo mejorar rendimiento UDF

10.  ⏳ **DataFrames - Windows**

    - Ventanas de tiempo - Windows

    - Window functions soportadas

    - Window specifications

    - Ejemplos

11.  🗃️ **Spark SQL - Tablas HIVE e Impala**

    - Spark contra tablas HIVE e Impala

    - Ejecutar queries con spark.sql()

12.  🧠 **Spark SQL - Funciones spark.SQL**

    - Funciones SQL específicas: `round`, `format_string`, `cast`, `trim`, `upper`

13.  🛠️ **Aplicación Spark**

    - Estructura de una aplicación Spark

    - Crear SparkSession y SparkContext (.builder)

    - Configurar logs (setLogLevel)

    - Cerrar la sesión

    - Comando para ejecutar desde CLI

    - Ejemplos (PySpark, Scala)

14.  🌊 **Procesar datos en streaming**

    - Procesar datos en streaming

    - Pasos

    - Formatos de salida

    - ".outputMode"

    - Compatibilidad entre Output Formats y Output Mode

    - Streaming Query

    - Ejemplos

15.  📡  **Kafka - CLI**

16.  🔌 **Kafka - Spark structured streaming**

    - Kafka en Spark

    - Modos de subscripción

    - Esquema de DataFrames de Kafka

    - Formato de mensaje común

    - Ejemplos

17. ⏳ **Sliding window aggregation**

    - Sliding window aggregation

    - Agregar datos por período de tiempo (window con micro-batches)

    - Uso de `functions.window`

    - Ejemplo

18.  📘 **DataSet**

19. ❄️ **Apache Iceberg**

    - Migración de tabla Hive (con HiveQL)

    - Importar tablas Hive a Iceberg

    - Migrar tablas de Hive a tablas Impala

    - Time travel (snapshot por ID)
