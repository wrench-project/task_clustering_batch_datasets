# Task Clustering Simulation Datasets
The datasets in this repository are used to evaluate task clustering algorithms for executing workflows on batch-scheduled HPC platforms using the simulator in the [task_clustering_batch_simulator repository](https://github.com/wrench-project/task_clustering_batch_simulator).

## Workflows

The [workflows](https://github.com/wrench-project/task_clustering_batch_datasets/tree/master/workflows) were synthetically generated using [this](https://confluence.pegasus.isi.edu/display/pegasus/WorkflowGenerator) open-source workflow generator. These workflows are generated based on four scientific application domains. Given those four workflow characterizations, we generated 4 * 3 * 3 = 36 workflow configurations by varying the number of tasks in each workflow and the total sequential duration of each workflow.

 Application | Number of tasks | Duration (hours) 
--- | --- | ---
 Cybershake, Epigenomics, Montage, Sipht| 50, 250, 500 | 100, 500, 1000
 
 The workflow files are named based on its workflow configuration using this scheme: APPLICATION_TASKS_DURATION.dax, where duration is in seconds. These files are in the 
 [DAX format](https://pegasus.isi.edu/documentation/creating_workflows.php). A path to one of theses workflow files is to be passed to the simulator as the  ```<workflow_specification>``` command-line argument.
 
## Workload Files
 
 The [workloads](https://github.com/wrench-project/task_clustering_batch_datasets/tree/master/workloads) are logs of real parallel workloads from various production systems. An expansive collection of these logs can be found in [SWF format](https://www.cse.huji.ac.il/labs/parallel/workload/swf.html) at the [Parallel Workloads Archive](https://www.cse.huji.ac.il/labs/parallel/workload/logs.html). The logs contained in this repository were downloaded off the archive. All logs in this repository are the "cleaned log -- RECOMMENDED" versions.
 
 Log File | System | Nodes
 --- | --- | ---
 kth_sp2.swf | KTH SP2 | 100
 sdsc_sp2.swf | SDSC SP2 | 128
 ctc_sp2.swf | CTC SP2 | 338
hpc2n.swf | HPC2n | 120

A path to one of these workload file is to be passed to the simulator as the ```<trace_file>```command-line argument (noting that the above number of nodes should be passed as the ```<compute_nodes>``` argument). 
 
