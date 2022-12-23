# Apache Spark - Class 1

### First We need to understand why Spark?

There are some Drawbacks in Hadoop MapReduce processing and then Spark came into the game.

The below points can be the most listed drawbacks of MapReduce:

1.  It's only made for Batch Processing
    
2.  CDC - Change Data Capture is not possible in MapReduce
    
3.  Slow processing - because of 'In memory' computation not implemented
    
    *   'In Memory' computation means utilising the memory as much as possible while processing.
        
4.  Not fault tolerant in terms of computation - If any failure occurs it will be starting from stage 1 and re-computation from the failure stage is not implemented.
    
5.  No mechanism implemented for caching persists.
    

To overcome the above points, we use Spark as our processing engine.

## Apache Spark

![Learn Apache Spark (Apache Spark Tutorials for Beginners) | by Hackr.io |  Hackr.io: Find the best online programming courses & tutorials | Medium](https://miro.medium.com/max/816/1*nzQpvE6QdEsPpBwhnXDqQg.png align="left")

*   It is a distributed computation framework.
    
*   It does not have any inbuilt file system or storage mechanism.
    

### Features of Spark

![Apache Spark Architecture | Distributed System Architecture Explained |  Edureka](https://www.edureka.co/blog/wp-content/uploads/2018/09/Picture5-2.png align="left")

1.  Speed - It is 100 times faster than Hadoop - This is officially proven.
    
2.  Powerful Caching - Capability to persist the data in memory while processing.
    
3.  Multiple Deploy method - We can deploy with the below Resource manager for Spark
    
    *   YARN
        
    *   Mesos
        
    *   Kubernetes
        
    *   Spark own cluster manager.
        
4.  Good fit for Batch and Real-time processing
    
5.  Polyglot - Spark provides high-level API for different languages - Python, Scala, Java and R.
    

## Spark Architecture

*   Spark follows Master-Slave architecture as Hadoop.
    
*   Spark Master Node
    
*   Spark Slave Nodes.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671253432822/8s3Jfwpic.png align="center")

### Client

*   Can be any machine from where we are sending our spark job for execution
    
*   Like Remote servers, web interfaces
    
    *   Spark shell - Used as an interactive shell - Available only in Python and Scala.
        
    *   Spark submit - when you have a complete spark application.
        

### Spark Master - Driver Program and Spark Context

#### Driver Program

*   It acts as the main method which will create Spark context.
    

#### Spark Context or Spark Session

*   It is the entry point to the spark core of the spark application.
    
*   It will connect our Spark App to the execution environment or cluster.
    
*   It creates a job execution graph and manages partitions, schedules etc.
    
*   Before Spark 2, Spark Context was used separately.
    
*   After Spark 2, the Spark session will do all things.
    

### Resource Manager

*   It will create one virtual container and start the Application master service in it.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671254484042/8fWxztf5Z.png align="center")
    
    *   The application Master will request to resource manager for complete resource allocation to start the required executors.
        
    *   Resource Manager will create the required number of executors for processing
        

#### Executors

*   Application masters and executors are virtual entity will have CPU, Memory and Network Bandwidth.
    
*   An executor does the actual computation on the partition Data.
    
*   Executors will start interacting with the Driver program for metadata and on-time job status updates.
    

Let us see this architecture with a small example to understand it deeply.

### Spark with YARN

let us assume we have Three worker nodes each have 256 GB Memory, 32 CPU cores

We need to execute two Spark jobs and one job needs 3 executors, each executor should have 5 CPU cores with 32 GB of memory. And another one needs 1 executor - 3 CPU cores with 32 GB memory.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671255748047/cQRfqx__w.png align="center")

Based on our requirements spark can assign the resources and execute the jobs as shown in the above flow.

**Now understand the CPU and task relationship:-**

In Map reduce we need one CPU core per map task. Same as that we need one CPU core per one spark task.

Task and CPU core are more important for executing jobs in parallel.

### Task

*   A small unit of execution is known as a task.
    
*   Each task will process one spark data partition.
    
*   One task will be executed on one CPU core.
    
*   One executor can run multiple tasks as per the available or assigned CPU cores.