---
layout: default
title: Computing resources
nav_order: 7
---
# Computing resources

**Seven condominium nodes on the Schooner supercomputer:**

- One A100 GPU node for production deep learning on the dual A100 GPUs
  - Dell PowerEdge R7525 (Nov. 2021)
  - CPUs: dual AMD EPYC Rome 7452 32-core
  - GPUs: dual NVIDIA A100 40 GB
  - RAM: 256 GB
  - Disk: dual 960 GB SSD vSAS, RAID1
  - Network: Infiniband HDR100 100 Gbps

- Five Cascade Lake node (nodes c657, c658, c659, c660 and c661) for parallel computing on the 200 CPU cores
  - Purpose: Parallel computing using the 200 CPU cores
  - Dell PowerEdge R640 (Jun. 2019)
  - CPUs: dual Intel Xeon Gold 6230 Cascade Lake 20-core
  - RAM: 192 GB
  - Disk: 800 GB SSD SATA
  - Network: Infiniband HDR100 100 Gbps

- One Skylake node (node c651) for applications with large memory requirement
  - Dell PowerEdge R440 (Nov. 2018)
  - CPUs: dual Intel Xeon Gold 6152 Skylake 22-core
  - RAM: 384 GB
  - Disk: dual 800 GB SSD SATA
  - Network: Infiniband FDR 56 Gbps

Useful instructions for using the condominium nodes

- [How to submit batch jobs](https://github.com/thepanlab/supercomputers/blob/master/Slurm_basics.md)
- [How to run the Jupyter notebooks](https://github.com/thepanlab/supercomputers/blob/master/Use_jupyter_notebook.md)
- How to manage your data and optimize the I/O

Thunder server for interactive deep learning on the dual RTX 3090 GPUs.

  - Lambda workstation (Dec. 2020)
  - CPUs: AMD Threadripper 3960X: 24 cores
  - GPUs: dual RTX 3090 24 GB
  - RAM: 128 GB
  - Disk: dual 2TB GB SSD
  - Network: Ethernet

Useful instructions for using the Thunder server

- [How to login and run the Jupyter notebook](https://github.com/thepanlab/supercomputers/blob/master/thunder/thunder_tensorflow_gpu_conda.md)
