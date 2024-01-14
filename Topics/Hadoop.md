# Hadoop - Short Notes 

> **Note:**
The below article is prepared for fair use with the help of resources published by [GeeksforGeeks](https://www.geeksforgeeks.org), [Alexsoft](https://www.altexsoft.com/blog/), and [Turing](https://www.turing.com/)

![image](https://github.com/elecsomk10/Demo/assets/37346017/7ebb9097-a620-466e-9159-3c67c380d1db)

### What is Hadoop?

There are mainly two problems with the big data.  
1. To **Store** a huge amount of data
2. To **Process** that stored data

The traditional approach like RDBMS is not sufficient due to the heterogeneity of the data. So, Hadoop comes as the solution to the problem of big data i.e. storing and processing the big data with some extra capabilities.

Hadoop is an open-source framework designed for the distributed storage and processing of large datasets using a cluster of commodity hardware. It's a part of the Apache Software Foundation and provides a set of tools and libraries for handling big data in a scalable and fault-tolerant manner.  
Hadoop is widely used for big data analytics, allowing organizations to efficiently store, process, and analyze massive volumes of structured and unstructured data. While Hadoop was initially the go-to solution for big data, newer technologies like Apache Spark have emerged, offering faster data processing capabilities. Nonetheless, Hadoop continues to be a foundational technology in the big data ecosystem.  
Hadoop serves as an excellent entry point for learning the basics of big data, offering a solid understanding of distributed storage, processing, and fault tolerance. As learners progress, exploring newer technologies complements this foundation and provides insights into the evolving landscape of big data solutions.

![Distributed Computers](https://github.com/elecsomk10/Blogs/assets/37346017/f7b8e375-e825-4411-b317-da9df686472b)

### History and Evolution of Hadoop

- In 2002, Doug Cutting and Mike Cafarella began Hadoop while working on Apache Nutch, an open-source web crawler aiming to build a search engine for a billion pages. Realizing their project's high costs, they sought a solution to handle large datasets more affordably.
- In 2003, inspired by Google's GFS paper, they found a solution for storing massive files but needed more.
- In 2004, Google's MapReduce paper provided the missing piece for processing large datasets. Recognizing the power of open source, Cutting and Cafarella implemented GFS and MapReduce in Nutch.
- In 2005, Cutting found that Nutch is limited to only 20-to-40 node clusters. He soon realized two problems:
  1. Nutch wouldn’t achieve its potential until it ran reliably on the larger clusters
  2. And that was looking impossible with just two people (Doug Cutting & Mike Cafarella).  
The engineering task in the Nutch project was much bigger than he realized. So, he started to find a job with a company that was interested in investing in their efforts. And he found Yahoo!. Yahoo had a large team of engineers that was eager to work on this project.  
- In 2006, Doug Cutting joined Yahoo along with the Nutch project. He wanted to provide the world with an open-source, reliable, scalable computing framework, with the help of Yahoo. So, at Yahoo first, he separated the distributed computing parts from Nutch and formed a new project Hadoop (He gave the name Hadoop it was the name of a yellow toy elephant that was owned by Doug Cutting’s son. and it was easy to pronounce and was the unique word.) Now he wanted to make Hadoop in such a way that it can work well on thousands of nodes. So, with GFS and MapReduce, he started to work on Hadoop.  
- In 2007, Yahoo successfully tested Hadoop on a 1000-node cluster and started using it.  
- In January 2008, Yahoo released Hadoop as an open-source project to ASF (Apache Software Foundation).
- In July 2008, Apache Software Foundation successfully tested a 4000-node cluster with Hadoop.  
- By 2009, Hadoop sorted a PetaByte of data in under 17 hours. Doug Cutting joined Cloudera to spread Hadoop's impact. 
- In 2011, Apache Hadoop version 1.0 was released, followed by version 2.0.6 in 2013. The latest release, Apache Hadoop version 3.0, came out in December 2017.

### Traditional Approach vs Hadoop Approach

In the traditional realm, data storage used to rely on local machines, a practice that served well until the datasets grew colossal. As data expanded beyond the capacity of local machines, a shift to remote servers became inevitable. However, a significant challenge emerged when processing this data. In the traditional enterprise approach, fetching sizable data, say 500 GB, from remote servers proved to be complex and costly. This is where Hadoop steps in with a game-changing approach. Instead of hauling data to local machines, Hadoop sends queries to where the data resides. The beauty lies in the query's size, which is significantly smaller than the massive dataset. Using the power of MapReduce, the server divides the query into parts, enabling parallel execution for simultaneous data processing. With Hadoop, there's no need to bear the burden of fetching extensive data, and the processing time is drastically reduced. The end result? A seamless process of storage, processing, and analysis, making Hadoop a transformative force in the world of data management compared to the traditional approach.  

![DBMS vs Hadoop](https://github.com/elecsomk10/Blogs/assets/37346017/c040e67f-4251-40f9-8054-6b4739ea42c3)

### Components of Hadoop

![Hadoop 1 vs Hadoop 2](https://github.com/elecsomk10/Demo/assets/37346017/f3f49a9e-cdca-4942-b359-68625adef204)

Core Components:
1. HDFS (Hadoop Distributed File Storage):  
   Role: HDFS is the **storage** backbone of Hadoop, designed for the distributed storage of large datasets across clusters.  
   How it Works: Data is divided into blocks and distributed across multiple nodes in the cluster, ensuring fault tolerance and scalability.  
   Key Feature: High fault tolerance allows HDFS to recover from node failures, ensuring data integrity.  
3. Map Reduce:  
   Role: MapReduce is the **processing engine** of Hadoop, enabling distributed data processing.  
   How it Works: It divides tasks into two phases - the Map phase for data processing and the Reduce phase for summarization. Tasks run parallelly across the cluster.  
   Key Feature: Parallel processing allows efficient handling of large datasets, making it a powerful tool for data transformation and analysis.  
5. YARN (Yet Another Resource Negotiator):  
   Role: YARN is the **resource management** layer that allocates resources and schedules tasks across the Hadoop cluster.  
   How it Works: YARN separates the resource management and job scheduling functions, allowing various applications to share resources efficiently.  
   Key Feature: Flexibility and improved utilization of resources, enabling Hadoop to support diverse workloads beyond MapReduce, such as Spark and Flink.  

In essence, HDFS provides a robust foundation for storing data across distributed nodes, MapReduce facilitates distributed processing, and YARN efficiently manages resources, collectively empowering Hadoop to handle massive datasets with scalability and fault tolerance. Beyond HDFS, YARN, and MapReduce, the entire Hadoop open-source ecosystem continues to grow and includes many tools and applications to help collect, store, process, analyze, and manage big data. These include Apache Pig, Apache Hive, Apache HBase, Apache Spark, Presto, and Apache Zeppelin.  

![Hadoop Ecosystem](https://github.com/elecsomk10/Demo/assets/37346017/88855e69-17d5-4ede-ac9b-a5a4e5b24e02)

![Hadoop Ecosystem Timeline](https://github.com/elecsomk10/Demo/assets/37346017/063b9d91-f4fb-43d8-9458-de8d13f9b2e7)

We can plug Hadoop with any of the storage systems: Local Storage/HDFS/Amazon S3  
We can plug Hadoop with any of the Resource Managers: YARN/MESOS/Kubernetes  
MapReduce processing unit can also be replaced by Spark in-memory processing framework.  

### How does Hadoop work? 

Hadoop allows for the distribution of datasets across a cluster of commodity hardware. Processing is performed in parallel on multiple servers simultaneously.  
Software clients input data into Hadoop. HDFS handles metadata and the distributed file system. MapReduce then processes and converts the data. Finally, YARN divides the jobs across the computing cluster.  
All Hadoop modules are designed with a fundamental assumption that hardware failures of individual machines or racks of machines are common and should be automatically handled in software by the framework.  

1. Data Storage with HDFS (Hadoop Distributed File System):  
   Data Division: Hadoop divides large datasets into smaller blocks (typically 128 MB or 256 MB in size).  
   Data Replication: Each block is replicated across multiple nodes in the Hadoop cluster (default replication factor is three), ensuring fault tolerance.  
2. Data Processing with MapReduce:  
   Map Phase:  
         a) Mapping: The MapReduce process begins with the Map phase where data is processed in parallel across nodes.  
         b) Key-Value Pairs: Data is transformed into key-value pairs based on specified mapping functions.  

   Shuffling:  
         a) Data Distribution: Key-value pairs are shuffled and redistributed across the cluster based on keys.  
         b) Grouping: Similar keys are grouped for the Reduce phase.  

   Reduce Phase:  
         a) Reducing: The Reduce phase aggregates and processes the grouped key-value pairs to generate the final output.  
4. Resource Management with YARN (Yet Another Resource Negotiator):  
   Resource Allocation: YARN manages resources in the Hadoop cluster by allocating memory and CPU to different applications.  
   Job Scheduling: It schedules tasks and coordinates the execution of applications, enabling multiple applications to share cluster resources efficiently.  
5. Execution Workflow:  
   User Submission: Users submit their MapReduce jobs to the Hadoop cluster.  
   JobTracker (in older versions) or ResourceManager (in YARN):  
   a) Task Assignment: JobTracker or ResourceManager assigns tasks to nodes.  
   b) Task Execution: TaskTracker (in older versions) or NodeManager (in YARN) executes tasks on individual nodes.  
   Result Retrieval: The results of the MapReduce job are collected and presented to the user.  
6. Data Locality Principle:  
   Efficient Processing: Hadoop follows the data locality principle, aiming to process data where it resides.  
   Reduced Data Transfer: By minimizing data transfer across the network, Hadoop enhances efficiency.  
7. Fault Tolerance:  
   Node Failure Handling: HDFS ensures fault tolerance by replicating data across nodes.  
   Task Re-execution: In case of node failure during processing, MapReduce tasks are re-executed on available nodes.  
8. Versatility and Ecosystem Integration:  
   Diverse Data Handling: Hadoop is designed to handle a variety of data types, including structured and unstructured.  
   Ecosystem Integration: Hadoop integrates with a rich ecosystem of tools (e.g., Hive, Pig, Spark) for different data processing and analytics needs.  

![How Hadoop Works?](https://github.com/elecsomk10/Demo/assets/37346017/b8de07bc-856c-470d-ace9-3eca9d99ef26)

### Benefits of Hadoop

1. Scalability
2. Low Cost
3. Flexibility
4. Fault Tolerance
5. High Availability

### Challenges of Hadoop 

1. MapReduce complexity and limitations: As a file-intensive system, MapReduce can be a difficult tool to utilize for complex jobs, such as interactive analytical tasks. MapReduce functions also need to be written in Java and can require a steep learning curve. The MapReduce ecosystem is quite large, with many components for different functions that can make it difficult to determine what tools to use.  
2. Security: Data sensitivity and protection can be issues as Hadoop handles such large datasets. An ecosystem of tools for authentication, encryption, auditing, and provisioning has emerged to help developers secure data in Hadoop.
3. Governance and Management: Hadoop does not have many robust tools for data management and governance nor data quality and standardization.
4. Talent Gap: Like many areas of programming, Hadoop has an acknowledged talent gap. Finding developers with the combined requisite skills in Java to program MapReduce, operating systems, and hardware can be difficult. In addition, MapReduce has a steep learning curve, making it hard to get new programmers up to speed on its best practices and ecosystem.
