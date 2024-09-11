## Introduction to Apache Spark: A Unified Analytics Engine

### The Genesis

#### Big Data and Distributed Computing at Google 

TBC

### What Is Apache Spark?

Apache Spark is a unified engine designed for large-scale distributed data processing, on premise in data centers or in the cloud. 

Spark provides in-memory storage for intermediate computations, making it much faster than Hadoop MapReduce. 

It composes libraries with composable APIs for machine learning (MLlib), SQL for interactive queries (Spark SQL), stream processing (Structured Streaming) for interacting with real-time data, and graph processing (GraphX).

Spark's design philosophy centers around four key characteristics:
1. Speed
    - Optimized for multi-core, multi-threaded systems with efficient parallel processing.
    - Uses DAG (Directed Acyclic Graph) scheduling and query optimization for efficient task execution across clusters.
    - Tungsten engine generates compact, efficient code for faster execution.
    - Retains intermediate results in memory, minimizing disk I/O for performance boosts.

2. Ease of Use
   - Simplifies big data processing with Resilient Distributed Datasets (RDDs), DataFrames, and Datasets.
   - Provides a straightforward programming model with familiar transformations and actions across multiple languages.
  
3. Modularity
   - Supports Scala, Java, Python, SQL, and R for diverse workloads.
   - Offers unified APIs with modules like Spark SQL, Structured Streaming, MLlib, and GraphX.
   - Combines multiple workloads under one engine for seamless processing without switching between engines or APIs.
  
4. Extensibility
   - Decouples computation from storage, unlike Hadoop, allowing integration with various data sources (e.g., HDFS, Cassandra, Hive, RDBMS).
   - Supports external sources like Kafka, Kinesis, Azure, and S3 via DataFrameReaders/Writers.
   - Rich ecosystem with connectors and tools for external data, monitoring, and more.

## Apache Spark Components as a Unified Stack

Spark offers four distinct components as libraries for diverse workloads: Spark SQL, Spark MLlib, Spark Strucutred Streaming, and GraphX. 

Each of these components is separate from Spark's core fault-tolerant engine, in that you use APIs to write your Spark application and Spark converts this into a DAG taht is executed by the core engine. 

So whether you write your Spark code using the provided Structured APIs in Java, R, Scala, SQL, or Python, the underlying code is decomposed into highly compact bytecode that is executed in the workers' JVMs across the cluster. 

![Apache Spark Components and API stack](https://github.com/user-attachments/assets/45db1e9a-2058-4ea8-a68c-4289237e5cb6 'Apache Spark Components and API stack')


1. Spark SQL
   - This module works well with structured data. You can read data stored in an RDBMS table or from file formats with structured data (CSV, text, JSON, Avro, ORC, Parquet, etc.) and then construct permanent or temporary tables in Spark.
   - When using Spark's Structured APIs in Java, Python, Scala or R, you can combine SQL-like queries to query the data just read into a Spark DataFrame.
   - Spark SQL is ANSI SQL:2003-compliant and it also functions as a pure SQL engine. 

2. Spark Structured Streaming
   - Apache Spark 2.0 introduced an experimental Continuous Streaming model and Structured Streaming APIs, built atop the Spark SQL engine and DataFrame-based APIs.
   - 




















