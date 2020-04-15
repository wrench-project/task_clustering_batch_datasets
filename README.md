# Task Clustering Simulation Datasets
These datasets are to facilitate the evaluation of task clustering algorithms on batch-scheduled HPC platforms using the simulator in the task_clustering_batch_simulator [repository](https://github.com/wrench-project/task_clustering_batch_simulator).

## Workflows
The [workflows](https://github.com/wrench-project/task_clustering_batch_datasets/tree/master/workflows) were synthetically generated using [this](https://confluence.pegasus.isi.edu/display/pegasus/WorkflowGenerator) open-source workflow generator. These workflows are generated based on four scientific application domains. Given those four workflow characterizations, we generated 4 * 3 * 3 = 36 workflows by varying the number of tasks in each workflow and the total sequential duration of each workflow.

 Application | Number of tasks | Duration (hours) 
--- | --- | ---
 Cybershake, Epigenomics, Montage, Sipht| 50, 250, 500 | 100, 500, 1000
 
 The workflow files are named based on its workflow configuration using this scheme: APPLICATION_TASKS_DURATION.dax, where duration is in seconds. These workflow files correspond to the "workflow_specification" argument of the task clustering simulator.
 
 ## Workload Files
 The [workloads](https://github.com/wrench-project/task_clustering_batch_datasets/tree/master/workloads) are logs of real parallel workloads from various production systems. An expansive collection of these logs can be found on the parallel workload [website](https://www.cse.huji.ac.il/labs/parallel/workload/logs.html). The logs contained in this repository were downloaded off the workload website and renamed to something shorter for simplicity. All logs in this repository are the "cleaned log -- RECOMMENDED" versions.
 Log File | System | Nodes
 --- | --- | ---
 kth_sp2.swf | KTH SP2 | 100
 sdsc_sp2.swf | SDSC SP2 | 128
 ctc_sp2.swf | CTC SP2 | 338
hpc2n.swf | HPC2n | 120

These workload files correspond to the "trace_file" argument of the task clustering simulator. The nodes correspond tot the "compute_nodes" argument of the task clustering simulator.
 
