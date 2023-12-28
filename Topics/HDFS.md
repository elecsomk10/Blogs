# HDFS

Before heading over to learn about the HDFS (Hadoop Distribution File System), we should know what the file system is.  
The File system is a kind of Data structure or method that we use in an operating system to manage files on disk space. This means it allows the user to maintain and retrieve data from the local disk.  
An example of the Windows file system is NTFS (New Technology File System) and FAT32 (File Allocation Table 32 bit).  
FAT32 is used in some older versions of Windows. Similarly, we have EXT3 and EXT4 kind of file systems for Linux OS. 

### What is DFS?

DFS stands for Distributed File System, it is a concept of storing the file in multiple nodes in a distributed manner.  
DFS provides the abstraction for a single large system whose storage is equal to the sum of storage of other nodes in a cluster.  
For example, Suppose we have a DFS comprised of 4 different machines each of size 10 TB in that case we can store let's say 30 TB across this DFS as it provides us a combined machine of size 40 TB. The 30 TB data is distributed among these nodes in the form of Blocks.  

![Distributed File System](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200728155638/Hadoop-HDFS-Hadoop-Distributed-File-System.png)

### Why do we need DFS?

You might be thinking that we can store a file of size 30 TB in a single system so why do we need this DFS?  
This is because the disk capacity of a system can only increase up to an extent. If somehow you manage the data on a single system, then you'll face the processing problem, processing large datasets on a single machine is not efficient.  
Let's understand this with an example. Suppose you have a file of size 40 TB to process. On a single machine, it will take suppose 4 hours to process it completely but what if you use a DFS? In that case, as you can see in the below image the File of size 40 TB is distributed among the 4 nodes in a cluster each node stores the 10 TB of file. As all these nodes are working simultaneously it will take only 1 Hour to completely process it which is the fastest, which is why we need DFS. 

Local File System Processing:  

![Local File System Processing](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200728155818/Local-File-System-Processing.png)

Distributed File System Processing: 

![Distributed File System Processing](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200728155848/Distributed-File-System-Processing.png)



