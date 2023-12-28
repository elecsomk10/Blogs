# Hadoop - Short Notes 

> **Note:**
The below article is prepared for fair use with the help of resources published by [GeeksforGeeks](https://www.geeksforgeeks.org), [Alexsoft](https://www.altexsoft.com/blog/), and [Turing](https://www.turing.com/)

![image](https://github.com/elecsomk10/Demo/assets/37346017/7ebb9097-a620-466e-9159-3c67c380d1db)

### What is Hadoop?

Hadoop is an open-source software developed for reliable, scalable, distributed computing.  
Written in Java and maintained by Apache.  
It is a framework that allows distributed processing of large data sets across clusters of computers using simple programming models.  
Designed to scale up from single servers to thousands of machines, each offering local computation and storage.  
Rather than rely on hardware to deliver high availability, the library itself is designed to detect and handle failures at the application layer, so delivering a highly-available service on top of a cluster of computers, each of which may be prone to failures.  
There are mainly two problems with the big data.  
1. To **Store** a huge amount of data
2. To **Process** that stored data
The traditional approach like RDBMS is not sufficient due to the heterogeneity of the data. So, Hadoop comes as the solution to the problem of big data i.e. storing and processing the big data with some extra capabilities.

![Distributed Computers](https://github.com/elecsomk10/Demo/assets/37346017/dc48307f-980e-4585-b3d1-8e8ccd759bca)

### History and Evolution of Hadoop

Hadoop was started by **Doug Cutting and Mike Cafarella** in the year 2002 when they both started to work on the Apache Nutch project. The Apache Nutch was  a highly extensible and scalable open-source web crawler project, that had the process of building a search engine system that can index 1 billion pages. After a lot of research on Nutch, they concluded that such a system will cost around half a million dollars in hardware, along with a monthly running cost of $30, 000 approximately, which is very expensive. So, they realized that their project architecture would not be capable enough to the workaround with billions of pages on the web. So, they were looking for a feasible solution that could reduce the implementation cost as well as the problem of storing and processing large datasets.  
In 2003, they came across a paper that described the architecture of Google’s distributed file system, called **GFS (Google File System)** which was published by Google, for storing large data sets. Now they realize that this paper can solve their problem of storing very large files that were being generated because of web crawling and indexing processes. But this paper was just the half solution to their problem.  
In 2004, Google published one more paper on the technique **MapReduce**, which was the solution for processing those large datasets. Now this paper was another half solution for Doug Cutting and Mike Cafarella for their Nutch project. These techniques (GFS & MapReduce) were just on white paper at Google. Google didn’t implement these two techniques. Doug Cutting knew from his work on Apache Lucene (It is a free and open-source information retrieval software library, originally written in Java by Doug Cutting in 1999) that open-source is a great way to spread the technology to more people. So, together with Mike Cafarella, he started implementing Google’s techniques (GFS & MapReduce) as open-source in the Apache Nutch project.  
In 2005, Cutting found that Nutch is limited to only 20-to-40 node clusters. He soon realized two problems:
(a) Nutch wouldn’t achieve its potential until it ran reliably on the larger clusters
(b) And that was looking impossible with just two people (Doug Cutting & Mike Cafarella).
The engineering task in the Nutch project was much bigger than he realized. So, he started to find a job with a company that was interested in investing in their efforts. And he found Yahoo!. Yahoo had a large team of engineers that was eager to work on this project.  
So, in 2006, Doug Cutting joined Yahoo along with the Nutch project. He wanted to provide the world with an open-source, reliable, scalable computing framework, with the help of Yahoo. So, at Yahoo first, he separated the distributed computing parts from Nutch and formed a new project Hadoop (He gave the name Hadoop it was the name of a yellow toy elephant that was owned by Doug Cutting’s son. and it was easy to pronounce and was the unique word.) Now he wanted to make Hadoop in such a way that it can work well on thousands of nodes. So, with GFS and MapReduce, he started to work on Hadoop.  
In 2007, Yahoo successfully tested Hadoop on a 1000-node cluster and started using it.  
In January of 2008, Yahoo released Hadoop as an open-source project to ASF (Apache Software Foundation). In July of 2008, Apache Software Foundation successfully tested a 4000-node cluster with Hadoop.  
In 2009, Hadoop was successfully tested to sort a PB (PetaByte) of data in less than 17 hours for handling billions of searches and indexing millions of web pages. Doug Cutting left Yahoo and joined Cloudera to fulfill the challenge of spreading Hadoop to other industries.  
In December of 2011, Apache Software Foundation released Apache Hadoop version 1.0. And later in Aug 2013, Version 2.0.6 was available. Currently, we have Apache Hadoop version 3.0 which was released in December 2017.  

Let's summarize the above History of Hadoop:

![History of Hadoop](https://github.com/elecsomk10/Demo/assets/37346017/becfb754-3617-4be2-b51c-85773ecb4cf3)

### Traditional Approach

In the traditional approach, we used to store data on local machines. This data was then processed. Now as data started increasing, the local machines or computers were not capable enough to store this huge data set. So, data was then started to be stored on remote servers. Now suppose we need to process that data. So, in the traditional approach, this data has to be fetched from the servers and then processed. Suppose this data is of 500 GB. Now, practically it is very complex and expensive to fetch this data. This approach is also called the Enterprise approach.  
In the new Hadoop approach, instead of fetching the data on local machines, we send the query to the data. The query to process the data will not be as huge as the data itself. Moreover, at the server, the query is divided into several parts. All these parts process the data simultaneously. This is called parallel execution and is possible because of Map Reduce. So, now not only there is no need to fetch the data, but also the processing takes less time. The result of the query is then sent to the user. Thus, Hadoop makes data storage, processing, and analyzing way easier than its traditional approach.  


![DBMS vs Hadoop](https://github.com/elecsomk10/Demo/assets/37346017/dda3bc7c-593c-4fb0-a361-268ee2d16755)

### Components of Hadoop

![Hadoop 1 vs Hadoop 2](https://github.com/elecsomk10/Demo/assets/37346017/f3f49a9e-cdca-4942-b359-68625adef204)

Core Components:
1. HDFS:  
   A Hadoop Hadoop-distributed File System is a dedicated file system to store big data with a cluster of commodity hardware or cheaper hardware with streaming access patterns. It enables data to be stored at multiple nodes in the cluster which ensures data security and fault tolerance.
   In our local PC, by default, the block size on the Hard Disk is 4 KB. When we install Hadoop, the HDFS by default changes the block size to 64 MB. Since it is used to store huge data. We can also change the block size to 128 MB. Now, HDFS works with Data Node and Name Node. While the Name Node is a master service and it keeps the metadata as for on which commodity hardware, the data is residing, the Data Node stores the actual data. Now since the block size is 64 MB the storage required to store metadata is reduced thus making HDFS better. Also, Hadoop stores three copies of every dataset at three different locations. This ensures that the Hadoop is not prone to a single point of failure.
2. Map Reduce:  
   Data once stored in HDFS also needs to be processed. Now suppose a query is sent to process a data set in the HDFS. Now, Hadoop identifies where this data is stored, this is called Mapping. Now the query is broken into multiple parts and the results of all these multiple parts are combined and the overall result is sent back to the user. This is called the reduce process. Thus, while HDFS is used to store the data, Map Reduce is used to process the data.  
   Most simply, it can be understood that MapReduce breaks a query into multiple parts and now each part processes the data coherently. This parallel execution helps to execute a query faster and makes Hadoop a suitable and optimal choice for dealing with Big Data.
3. YARN (Yet Another Resource Negotiator):  
   It is a dedicated operating system for Hadoop which manages the resources of the cluster and also functions as a framework for job scheduling in Hadoop. The various types of scheduling are First Come First Server, Fair Share Scheduler Capacity Scheduler, etc. The First Come First Serve scheduling is set by default in YARN.
   As we know YARN works like an OS to Hadoop and as OS are resource managers YARN manages the resources of Hadoop so that Hadoop serves big data in a better way.  
Beyond HDFS, YARN, and MapReduce, the entire Hadoop open-source ecosystem continues to grow and includes many tools and applications to help collect, store, process, analyze, and manage big data. These include Apache Pig, Apache Hive, Apache HBase, Apache Spark, Presto, and Apache Zeppelin.  

![Hadoop Ecosystem](https://github.com/elecsomk10/Demo/assets/37346017/88855e69-17d5-4ede-ac9b-a5a4e5b24e02)

![Hadoop Ecosystem Timeline](https://github.com/elecsomk10/Demo/assets/37346017/063b9d91-f4fb-43d8-9458-de8d13f9b2e7)

We can plug Hadoop with any of the storage systems: Local Storage/HDFS/Amazon S3
We can plug Hadoop with any of the Resource Managers: YARN/MESOS/Kubernetes
MapReduce processing unit can also be replaced by Spark in-memory processing framework. 

### How does Hadoop work? 

Hadoop allows for the distribution of datasets across a cluster of commodity hardware. Processing is performed in parallel on multiple servers simultaneously.  
Software clients input data into Hadoop. HDFS handles metadata and the distributed file system. MapReduce then processes and converts the data. Finally, YARN divides the jobs across the computing cluster.  
All Hadoop modules are designed with a fundamental assumption that hardware failures of individual machines or racks of machines are common and should be automatically handled in software by the framework.  

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
3. Governance and Management: Hadoop does not have many robust tools for data management and governance nor for data quality and standardization.
4. Talent Gap: Like many areas of programming, Hadoop has an acknowledged talent gap. Finding developers with the combined requisite skills in Java to program MapReduce, operating systems, and hardware can be difficult. In addition, MapReduce has a steep learning curve, making it hard to get new programmers up to speed on its best practices and ecosystem.
