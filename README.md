## All About Big Data



### 1. What are 5 V's of data?
 
The 5 V's of Big Data are a set of characteristics that describe the challenges and dimensions of big data. 
The 5 V's are:

* **Volume:** 
Refers to the sheer size of the data being generated and collected. 
Big data involves datasets that are too large to be comfortably processed by traditional database systems. 
It often involves terabytes, petabytes, or even larger quantities of data.

* **Velocity:**
Describes the speed at which data is being generated, collected, and processed. 
With the proliferation of real-time systems, IoT devices, and social media, data can be generated at an unprecedented speed. 
This requires the ability to process and analyze data streams in near real-time.

* **Variety:** 
Represents the diverse types of data that are being generated. 
Data comes in many formats, including structured data (like databases), unstructured data (like text or images), 
and semi-structured data (like JSON or XML). 
Big data systems need to be able to handle this variety efficiently.

* **Variability:** 
Refers to the inconsistency in the data's format, quality, and meaning. 
Data sources might have different structures, missing values, or inaccuracies. 
Big data systems must be able to handle and process such variability effectively.

* **Veracity:** 
Relates to the trustworthiness and reliability of the data. 
With the large volume of data being generated from multiple sources, ensuring data quality and accuracy becomes a significant challenge. 
It's important to have mechanisms in place to validate and ensure the correctness of the data.

Some of the other important V's include: 

* **Value:** 
Highlighting the importance of deriving meaningful insights and value from the data. 
Collecting and processing data is valuable only if it leads to actionable insights and informed decision-making.

* **Validity:** 
Emphasizing the necessity of ensuring that the data is valid, accurate, and trustworthy.

* **Volatility:** 
Referring to the temporary nature of certain data streams or the rapid changes in data over time.
-------------------------------------------------
### 2. What is big data?
Big data refers to extremely large and complex datasets that cannot be easily managed, processed, or analyzed using traditional data processing tools and methods. These datasets are characterized by their volume, variety, velocity, and sometimes veracity.

The concept of big data has gained prominence due to advancements in technology, such as increased storage capacities, faster processing capabilities, and improved data analytics techniques. Organizations and researchers use big data analytics to extract valuable insights, trends, patterns, and correlations from these massive datasets. These insights can help with making informed decisions, improving business strategies, enhancing scientific research, and more.

To process and analyze big data effectively, specialized tools and technologies have emerged, such as distributed computing frameworks (like Hadoop), NoSQL databases, data lakes, and machine learning algorithms. These tools enable organizations to handle the challenges posed by the enormous amounts of data generated in today's digital world.


-------------------------------------------------
### 3. What is Apache Hadoop? Also mention its versions.
Apache Hadoop is an open-source framework designed for storing and processing large datasets in a distributed computing environment. It was created to address the challenges of handling big data, which involves massive volumes of data that cannot be easily managed or processed using traditional methods.


The core components of Apache Hadoop include:
* **Hadoop Distributed File System (HDFS):**
HDFS is a distributed file system that allows large datasets to be stored across multiple servers (nodes) in a cluster. It divides files into smaller blocks and replicates them across different nodes for fault tolerance. This architecture enables efficient data storage and retrieval.

* **MapReduce:**
MapReduce is a programming model and processing engine that allows developers to write programs for processing and analyzing large datasets in parallel across a distributed cluster. It simplifies the process of breaking down complex tasks into smaller tasks that can be executed concurrently.

* **YARN (Yet Another Resource Negotiator)**
YARN is a resource management and job scheduling component in Hadoop. It manages and allocates resources to different applications running on the cluster, enabling efficient utilization of cluster resources.

* **Hadoop Common:**
This includes libraries, utilities, and APIs used by various Hadoop modules. It provides a consistent and shared infrastructure for Hadoop components.

* **Hadoop Ecosystem**
Apart from the core components, the Hadoop ecosystem consists of various complementary projects and tools that extend the capabilities of Hadoop. These include tools for data ingestion (Apache Flume, Apache Kafka), data processing (Apache Pig, Apache Hive), data querying (Apache Drill, Apache Impala), and more.



Following are the versions introduced by Apache Hadoop:

* **Hadoop 1.x (2006-2012):**
  The initial release of Hadoop focused on introducing the Hadoop Distributed File System (HDFS) and the MapReduce programming model. It provided a scalable way to process and store large datasets across clusters of commodity hardware.

* **Hadoop 2.x (2012-2013):**
  Hadoop 2 marked a significant shift with the introduction of YARN (Yet Another Resource Negotiator). YARN separated resource management from job scheduling, allowing for more diverse processing frameworks beyond MapReduce. This enabled Hadoop to support a wider range of applications.

* **Hadoop 3.x (2017-present):**
  Hadoop 3 brought further improvements to resource management and added support for erasure coding in HDFS, reducing storage overhead. It also introduced improvements to support larger clusters, more efficient data processing, and enhanced security features.
 
-------------------------------------------------
### 4. What is GFS - Google File System?
The Google File System (GFS) is a proprietary distributed file system developed by Google to manage and store large amounts of data across clusters of commodity hardware. It was designed to meet Google's specific needs for handling vast amounts of data efficiently and reliably, and it served as a foundation for many of Google's services, including Google Search, Google Maps, and Gmail.


Key characteristics of the Google File System include:

* **Scalability:** GFS is designed to scale to accommodate enormous amounts of data. It achieves this by distributing data across multiple storage servers in a cluster, enabling the system to handle petabytes of data across thousands of machines.

* **Fault Tolerance:** GFS is built to operate on commodity hardware, which is prone to failures. It addresses this challenge through data replication. Files are divided into fixed-size chunks, and each chunk is replicated across multiple machines. If one machine fails, the system can retrieve the data from another replica.

* **Simplified Interface:** GFS provides a simplified file system interface, optimized for large files and streaming reads and writes. It sacrifices certain features found in traditional file systems to achieve greater performance and efficiency for Google's workloads.

* **Data Locality:** GFS is designed to take advantage of data locality, meaning that data is stored close to the computation that needs it. This reduces network congestion and speeds up data processing.

* **Master-Chunkserver Architecture:** GFS architecture includes a single master server that manages metadata (such as file namespaces, access control, and location information) and multiple chunk servers responsible for storing and serving data chunks.

It's important to note that GFS is not open source and is proprietary to Google. However, its design principles and concepts have influenced the development of various open-source distributed file systems and storage solutions, including the Hadoop Distributed File System (HDFS) and other similar systems.


### Comparison of GFS / HDFS
The Google File System (GFS) and Hadoop Distributed File System (HDFS) are both distributed file systems designed to manage and store large datasets across clusters of commodity hardware. They share many similarities in terms of goals and design principles, but they were developed by different organizations and serve as foundations for different ecosystems.

Here's a comparison between GFS and HDFS:

* Origin and Purpose:
  
   GFS: Developed by Google for its internal use, GFS was designed to handle Google's massive data storage and processing needs for services like Google Search and Gmail.

  HDFS: HDFS is an open-source project that is part of the Apache Hadoop ecosystem. It was created to provide similar capabilities as GFS and is used for storing and processing big data in a distributed manner.

* Architecture:
  
   Both GFS and HDFS use a master-chunkserver architecture, where there's a master server responsible for metadata management and multiple chunk servers responsible for storing data blocks/chunks.

* Scalability:
  
   Both systems are designed to handle the massive scale required by modern data processing. They achieve scalability by distributing data across a large number of commodity hardware nodes.

* Fault Tolerance:
  
   Both systems address hardware failures and ensure data availability through data replication. Data chunks are replicated across multiple nodes to provide fault tolerance.

* Data Locality:
  
   Both GFS and HDFS are designed to optimize data locality. Data is stored near the computation that needs it, reducing network traffic and improving performance.

* Open Source:
  
  GFS: Google's GFS is a proprietary system and is not publicly available.
  
  HDFS: HDFS is open source and part of the Apache Hadoop project, making it accessible to a wide community of users and developers.

* Ecosystem:
  
   GFS: GFS served as the inspiration for the development of various distributed file systems, including HDFS.

  HDFS: HDFS is a fundamental component of the Apache Hadoop ecosystem, which includes a wide range of tools and frameworks for data storage, processing, and analysis, such as MapReduce, YARN, and various data processing libraries.


In summary, the Google File System (GFS) and Hadoop Distributed File System (HDFS) are similar in their goals of providing scalable and fault-tolerant storage for large datasets. While GFS was developed by Google for its internal use, HDFS emerged as an open-source project within the Apache Hadoop ecosystem and has become a central component in the big data landscape.


-------------------------------------------------
5. What is YARN in hadoop context?

-------------------------------------------------
6. What is MapReduce ? Solve an example also.

-------------------------------------------------
7. What is Apache Tez?

-------------------------------------------------
8. What is Apache Spark?

-------------------------------------------------
9. Compare MapReduce / Tez / Spark 

-------------------------------------------------
10. What is PIG in hadoop context?

-------------------------------------------------
11. What is Sentry?

-------------------------------------------------
12. What is ZOOKEEPER in hadoop context?

-------------------------------------------------
13. What is Spark MLlib?

-------------------------------------------------

