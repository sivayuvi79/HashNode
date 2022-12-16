# Apache Spark Introduction

### First We need to understand why Spark?

There are some Drawbacks in Hadoop MapReduce processing and then Spark came into the game.

The below points can be the most listed drawbacks of MapReduce:

1.  It's only made for Batch Processing
    
2.  CDC - Change Data Capture is not possible in MapReduce
    
3.  Slow processing - because of 'In memory' computation not implemented
    
    *   'In Memory' computation means utilising the memory as much as possible while processing.
        
4.  Not fault tolerant in terms of computation - If any failure occurs it will be starting from stage 1 and re-computation from the failure stage is not implemented.
    
5.  No mechanism implemented for caching, persists.
    

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
    

## Spark Architecture:

*   Spark follows Master-Slave architecture as Hadoop.
    
*   Spark Master Node
    
*   Spark Slave Nodes.