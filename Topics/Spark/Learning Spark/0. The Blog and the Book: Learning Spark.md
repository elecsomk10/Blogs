## A Journey with "Learning Spark"

In my journey to master Apache Spark, I’ve turned to “Learning Spark” *(published by O'Reilly Media)*, co-authored by Matei Zaharia and key contributors from Databricks. This book is an invaluable resource for anyone looking to dive into distributed data processing with Spark, as it covers everything from fundamental concepts to advanced features.

In the following blog posts, I’ll be sharing my learnings and insights as I explore the content of this book. I highly recommend reading the book itself, as it offers a deep dive into Spark’s architecture, development history, and practical applications. The examples and explanations provided by the authors are well-structured and serve as a solid foundation for both beginners and experienced developers alike.

By sharing my notes and key takeaways here, I hope to create a supplementary guide for fellow learners while encouraging anyone interested in Spark to refer directly to this excellent resource for more comprehensive coverage.

You can access “Learning Spark” for free from the Databricks website [here](https://pages.databricks.com/rs/094-YMS-629/images/LearningSpark2.0.pdf "Learning Spark book").

### Who This Book Is For

For Data Engineers,
- learn how to use Spark's Structured APIs to perform complex data exploration and analysis on both batch and streaming data
- use Spark SQL for interactive queries
- use Spark's built-in and external data sources to read, refine, and write data in different file formats as part of their extract, transform, and load (ETL) tasks
- build reliable data lakes with Spark and the open-source Delta Lake table format

For Data Scientists and Machine Learning Engineers, 
- Spark's MLlib library offers many common algorithms to build distributed machine learning models
- covers how to build pipelines with MLlib, best practices for distributed machine learning
- how to use Spark to scale single-node models, and how to manage and deploy these models using the open-source library MLflow

Finally, because Spark is a distributed engine, building an understanding of Spark application concepts is critical. This will guide you through how your Spark application interacts with Spark's distributed components and how execution is decomposed into parallel tasks on a cluster. It also covers which deployment modes are supported and in what environments. 


### What Is Covered In “Learning Spark”

1. Introduction to Apache Spark: A Unified Analytics Engine  
2. Downloading Apache Spark and Getting Started
3. Apache Spark's Structured APIs
4. Spark SQL and DataFrames: Introduction to Build-in Data Sources
5. Spark SQL and DataFrames: Interacting with External Data Sources
6. Spark SQL and Datasets
7. Optimizing and Tuning Spark Applications
8. Structured Streaming
9. Building Reliable Data Lakes with Apache Spark
10. Machine Learning with MLlib
11. Managing, Deploying, and Scaling Machine Learning Pipelines with Apache Spark
12. Epilogue: Apache Spark 3.0

### Software and Configuration

By the time this blog is published,
- Apache Spark 3.0
- Java Development Kit (JDK) 1.8.0

If you intend to use only Python, then you can simply run `pip install pyspark`.

