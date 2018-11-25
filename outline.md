# Abstract

Data-intensive computing has become increasingly important because of the demand to extract pattern and knowledge from the extreme large volume of data.  In parallel with this trend, cloud computing has become a vital infrastructure for hosting services because users are able to pay for what they actually need and to choose resource configurations to fit their service requirements. However, hosting data-intensive applications on the cloud has several challenges such as I/O performance efficiency and guarantee of storage services. Furthermore, it is not trivial to choose the most cost-effective cloud configurations for applications demanding large data sizes or high I/O operations.

In this dissertation, we aim to make data-intensive computing more efficient and reliable running on the cloud.

First, we present Inside-Out, an automatic model building tool that creates accurate performance models for distributed storage services.

Second, we propose a novel flow scheduling method for the MapReduce framework to eliminate I/O bottleneck while improving execution time.

Third, we present Rainbow, a fine-grained, workload-aware data replication and placement scheme, for efficient cloud elasticity.		

Last, we plan to develop a cost and performance model that chooses resource and software configurations automatically for running large-scale data processing applications on the cloud.	


# I. Introoduction

Data-intensive computing is extremely important because the ever-increasing data can generate information that improves and even transforms our daily life.

* Deninition: I/O bound, large dataset, etc.
* Characteristics: 4V (volume, variaty, velocity and veracity)
* Instances: programming models (mapreduce, graph, etc.), systems (Hadoop, HPCC)
* Challenges: to provide efficient systems for intensive computing and massive storage



Cloud computing, specifically the infrastructure-as-a-service (IaaS), allows one to lease and manage computing infrastructure and shifts costs from captital expenditure to operational expense — the pay-as-you-go model.

* Motivation: demand is unpredictable or highly variable
* Characteristics: pay-as-you-go, elasticity, configurability
* Challenges: performance unpredictability, cost-effective configurations, etc.

Hosting data-intensive applications on the cloud is promising but encouters great challenges.

* Advantages
  * Solve very large-scale problems
  * Elastic resource scaling enables the application to cope with unpredictable or highly variable workload
  * Mature eco-system for machine-learning cloud-based services
* Challenges
  * **General**: guaranteeing performance (**workload**, **elasticity**, re**configuration**, **multitenancy**), *balancing computation and I/O requrests* (**elasticity**, dynamic **workload**), optimizing configurations (**configuration**, **storage** choices, cost-performance tradeoff)

We tackle these important challenges of running data-intensive applications on the cloud.

* **Storage** Hard to guarantee the performance of a distributed storage system due to dynamic workload, elastic scaling, changing SLO, performance interference by multi-tenancy
* **Platform** Systems are designed for the reference architecture but not remote storage or cloud storage. Balancing I/O requests is a crititcal issue.
* **Platform** Efficient resizing a cluster requires proper data replication and placement to match the anticipated workload.
* **Cost** Searching for the most cost-effective configurations requires a comprehensive/clear/good undersanding of resource capability and application characteristics.







## Contribution



Hint: approach and its results

1. Inside-Out: an automatic end-to-end performance model building tool for distributed storage systems
   * Estimate end-to-end performance of a distributed storage system using only low-level performance metrics collected from indivisual machines.
   * A black-box approach that does not require knowledge about system configurations and workload characteristics.
   * A two-level learning method that eliminates irrelevant features while avoiding overfitting problems.
   * Accurate: achieves 91.1% prediction accuracy on average.
   * Consistent: dynamic workload, reconfiguring systems, performance interference by multi-tenancy
   * Online self-learning automatically corrects over- and under-prediction errors
2. Flow Scheduling: a novel scheduling method that balances I/O demands for the MapReduce system
   {0}. Model the job scheduling in MapReduce as a minimum cost network optimization problem
   {0}. Improves the system throughput by 30%.
   {0}. Eliminates stragglers (slow map or reduce tasks) by avoiding resource contention	
3. Rainbow: distribution-aware data replication and placement for efficient cloud elasticity.
   * Explore how partition granularity affects system performance
   * Rainbow improves system performance by 76% for system throughput and 31% for query latency under the common power law workload.
   * Rainbow is more robust to accomodate slightly mis-predicted workloads.
   * Rainbow outperform the corase-grained scheme when the cluster size expands or contracts.



# II. Background

## Data-Intensive Computing

### MapReduce
### Apache Hadoop
### High-Performance Computing Cluster (HPCC Systems)


## Cloud Elasticity and Configurations
### Elasticity
### Resource Configurations

## Software-Defined Storage (Distributed Storage Systems)

### SDS Scenario
### Ceph
### Hadoop Distributed File System (HDFS)



## Storage Models for Data-Intensive Computing

### Reference Model
### Remote Storage Model
### Cloud Storage Model
### Storage Tier (offline vs online storage)


# III. Inside-Out: End-to-End Performance Prediction for Cloud Storage

# IV. Flow-Aware Job Scheduling

# V. Workload-Aware Data Placement

# VI. Exploring Time-Cost Tradeoff on the Cloud

# VII. Concluding



