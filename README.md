# Cloud Computing for Science 2021/2022

This tutorial aims to replicate a Bloomberg analysis concerning mortgage costs in the United States by distributing the computation workload over a small Apache-Spark cluster deployed on Chameleon. The study is focused on the disparity between racial groups and how it is exacerbated by non-bank lenders. Data is retrieved from the Home Mortgage Disclosure Act database, a comprehensive collection of the mortgage maker activities that lender providers report to their regulators. For this study, some multiple linear regression analyses are needed, as well as a preprocessing phase aimed at filtering and cleaning the data.

Even though the dataset size may not require distributed computation across multiple nodes, the deployment of a small cluster can be seen as an exercise and preparation for scaling up the project. Moreover, even with a single node environment, Spark provides a boost in performance, if compared to native Python or R scripts, thanks to its built-in parallelization and optimization engine.

The cluster setup will consist of three virtual machines managed by OpenStack: one master node and two workers. For distributing the data across the nodes and coordinating the jobs, the Hadoop Distributed File System (HDFS) and YARN will be used.
