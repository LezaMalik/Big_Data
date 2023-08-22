## All About Big Data : Hadoop



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

### 5. What is YARN in hadoop context?
YARN stands for "Yet Another Resource Negotiator," is a key component in the Apache Hadoop ecosystem. It was introduced in Hadoop 2.x to address limitations in the original Hadoop MapReduce framework's resource management and job scheduling capabilities. YARN essentially separates the resource management and job scheduling aspects, enabling Hadoop to support a broader range of processing frameworks beyond just MapReduce.

In the context of Hadoop, YARN serves as a resource management layer that efficiently allocates and manages resources across a cluster, enabling different applications to run concurrently and share cluster resources effectively. 

Here's how YARN works within the Hadoop ecosystem:

* **Resource Management:** YARN manages the physical resources (CPU, memory, etc.) of the cluster's nodes. It keeps track of available resources and allocates them to applications as needed. This enables multi-tenancy, allowing various applications to coexist on the same cluster without negatively impacting each other.

* **Application Management:** YARN allows multiple applications to run on the same cluster simultaneously. Each application runs within its own application master, which is responsible for managing its tasks, monitoring progress, and negotiating resource requirements.

* **Job Scheduling:** YARN's ResourceManager handles the allocation of resources based on the resource requirements of applications. It makes scheduling decisions based on fairness and capacity, ensuring optimal resource utilization across the cluster.

* **NodeManager:** Each node in the cluster runs a NodeManager process, responsible for monitoring resource usage on the node and reporting this information to the ResourceManager. It also manages the execution of tasks requested by the ApplicationMaster.

With YARN, Hadoop clusters became more versatile and efficient. In addition to running MapReduce jobs, Hadoop 2.x and later versions can host various other processing frameworks that can share resources in a more flexible manner. This enables a wide range of applications, including real-time data processing (like Apache Spark and Apache Flink), interactive querying (like Apache Tez), and more, to be seamlessly integrated into the Hadoop ecosystem.


-------------------------------------------------

### 6. What is MapReduce ? Solve an example also.

MapReduce is a programming model and processing paradigm designed for processing and generating large-scale datasets across distributed computing clusters. It was popularized by Google and became a fundamental concept in the Hadoop ecosystem. The idea behind MapReduce is to break down a complex data processing task into smaller subtasks that can be executed in parallel across multiple nodes in a cluster.

The MapReduce model consists of two main phases: the "Map" phase and the "Reduce" phase.

* **Map Phase:**
 In this phase, the input data is divided into chunks, and each chunk is processed independently by a "Map" function. The "Map" function takes the input data, applies a transformation to it, and emits key-value pairs as intermediate output.

* **Shuffle and Sort:**
 After the "Map" phase, the intermediate key-value pairs are shuffled and sorted based on their keys. This step groups together all intermediate values associated with the same key, preparing the data for the next phase.

* **Reduce Phase:**
 In the "Reduce" phase, the shuffled and sorted intermediate key-value pairs are processed by the "Reduce" function. The "Reduce" function takes a key and a list of values associated with that key, applies some computation to those values, and generates final output data.

**Example:**

Problem: *Calculate the average score of students from a dataset containing student names and their corresponding scores.*

**Map Phase:**

Input: 
    
    ("Alice", 85), ("Bob", 92), ("Alice", 78), ("Bob", 90), ("Charlie", 75)

Map Function:

    Map("Alice", 85) -> ("Alice", 85)
    
    Map("Bob", 92) -> ("Bob", 92)
    
    Map("Alice", 78) -> ("Alice", 78)
    
    Map("Bob", 90) -> ("Bob", 90)
    
    Map("Charlie", 75) -> ("Charlie", 75)

Shuffle and Sort:

Intermediate Key-Value Pairs: 

    ("Alice", [85, 78]), ("Bob", [92, 90]), ("Charlie", [75])



**Reduce Phase:**

Reduce Function:
 
    Reduce("Alice", [85, 78]) -> ("Alice", 81.5)
    
    Reduce("Bob", [92, 90]) -> ("Bob", 91.0)
    
    Reduce("Charlie", [75]) -> ("Charlie", 75.0)

**Output:**

    "Alice" has an average score of 81.5.
    
    "Bob" has an average score of 91.0.
    
    "Charlie" has an average score of 75.0.


In this example, the MapReduce paradigm effectively calculates the average score for each student by distributing the data processing across multiple nodes and aggregating the results.
   

-------------------------------------------------

### 7. What is Apache Tez?
Apache Tez is an open-source framework built on top of Apache Hadoop YARN (Yet Another Resource Negotiator). Tez aims to improve the efficiency and performance of data processing tasks in the Hadoop ecosystem by providing a more flexible and optimized execution engine. It enables faster and more interactive processing of big data workloads by optimizing the execution of complex directed acyclic graph (DAG) workflows.

Tez addresses some limitations of the original MapReduce model, such as its reliance on a two-phase execution model (Map and Reduce) and its lack of support for complex data processing tasks. Tez introduces a more generalized execution framework that allows users to express arbitrary data processing logic as directed acyclic graphs. This enables complex workflows involving multiple stages and different types of operations to be executed more efficiently.

Key features of Apache Tez include:

* **DAG Execution:** Tez enables the execution of complex data processing workflows represented as directed acyclic graphs (DAGs). These DAGs can include multiple stages of computation, data transformations, joins, aggregations, and more.

* **Efficient Data Movement:** Tez optimizes data movement between tasks, minimizing the amount of data shuffled across the cluster. This reduces the overall processing time and improves performance.

* **Task-level Optimization:** Tez supports task-level optimization, allowing tasks to be dynamically optimized based on data characteristics and execution history. This helps in reducing execution time and resource consumption.

* **User-Defined Functions:** Tez supports custom user-defined functions, enabling developers to express their specific processing logic within DAG workflows.
  
* **Broad Ecosystem Integration:** Tez is designed to work with a variety of data processing frameworks. It can be used as an execution engine for Hive (a data warehousing and SQL-like querying tool), Pig (a data flow language for data processing), and other compatible tools.

* **Compatibility with YARN:** Tez is built on top of YARN, making it compatible with Hadoop clusters and allowing it to leverage YARN's resource management capabilities.

* **Efficient Resource Utilization:** Tez optimizes the utilization of cluster resources by reducing data movement and enabling better sharing of resources among tasks.


-------------------------------------------------

### 8. What is Apache Spark?
Apache Spark is an open-source, distributed computing framework designed for processing and analyzing large-scale data sets. It's a part of the broader big data ecosystem, often used in conjunction with Hadoop, but it can also work independently of Hadoop's HDFS (Hadoop Distributed File System). Apache Spark aims to provide a more efficient and flexible alternative to the traditional MapReduce processing model used in Hadoop.

Key features of Apache Spark:

* **In-Memory Processing:** Spark performs much of its data processing in memory, reducing the need to read and write intermediate results to disk. This leads to significant performance improvements compared to Hadoop's MapReduce, which involves more disk I/O.

* **Ease of Use:** Spark offers APIs in several programming languages (Scala, Java, Python, and R), making it more accessible for developers with different skill sets. This enables more complex data processing tasks without needing to write extensive low-level code.

* **Resilient Distributed Datasets (RDDs):** RDD is the fundamental data structure in Spark. It's an immutable distributed collection of objects that can be processed in parallel. RDDs provide fault tolerance through lineage information, enabling lost data to be reconstructed in case of node failures.

* **Data Transformation and Analysis:** Spark provides a rich set of operators for data transformation and analysis, such as map, reduce, filter, join, and more. These operators allow developers to express complex data processing pipelines more intuitively.

* **Spark SQL:** Spark includes a module for processing structured and semi-structured data using SQL queries. This makes it easier for analysts and data scientists familiar with SQL to work with big data.

* **Machine Learning and Graph Processing:** Spark's MLlib library offers machine learning algorithms that can work with large datasets. Additionally, GraphX provides a graph processing library for graph-based data analysis.

* **Streaming:** Spark Streaming allows real-time processing of data streams. This is useful for applications like monitoring social media, processing log files, or real-time analytics.

* **Cluster Manager Integration:** Spark can be integrated with various cluster managers, such as Apache Hadoop YARN, Apache Mesos, or it can be run in standalone mode.


While Spark can be used independently, it's often employed alongside Hadoop, where HDFS is used as a storage layer for the data and Spark is used for more efficient and faster data processing. This combination leverages the strengths of both frameworks, utilizing Spark's in-memory processing and Hadoop's distributed storage capabilities.


Overall, Apache Spark is a powerful tool in the big data landscape, enabling organizations to process and analyze vast amounts of data more efficiently and with more flexibility than traditional approaches like MapReduce.


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

