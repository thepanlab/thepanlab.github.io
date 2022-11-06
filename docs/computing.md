---
layout: default
title: Computing
nav_order: 6
---
# Computing Resources

### **Condominium nodes on the [Schooner](https://www.ou.edu/oscer/resources/hpc) supercomputer:**

- **One dual-A100 GPU node** (Nov. 2021)  
  For deep learning on two A100 GPUs.  
  Node ID: TBD.   
  CPUs: dual 32-core AMD EPYC Rome 7452.   
  GPUs: dual NVIDIA A100 40 GB.  
  RAM: 256 GB.  
  Disk: dual 960 GB SSD vSAS, RAID1.  

- **Five Cascade Lake nodes** (Jun. 2019)   
  Node ID: c657, c658, c659, c660 and c661.  
  CPUs: dual 20-core Intel Xeon Gold 6230 Cascade Lake.   
  RAM: 192 GB.  
  Disk: 800 GB SSD SATA.  

- **One Skylake node** (Nov. 2018)  
  Node ID: c651.  
  CPUs: dual 22-core Intel Xeon Gold 6152 Skylake.   
  RAM: 384 GB   
  Disk: dual 800 GB SSD SATA.  

#### How to use the condominium nodes
  - [How to submit batch jobs to our partition](https://github.com/thepanlab/supercomputers/blob/master/Slurm_basics.md)
  - [How to run Jupyter notebooks on our nodes](https://github.com/thepanlab/supercomputers/blob/master/Use_jupyter_notebook.md)

### **Data storage:**
  - local SSD space on compute nodes (/lwork)
  - 2 TB disk space on parallel file system (/work/omicsbio)
  - 10 TB tape archival space

  [How to manage the data and optimize the I/O](https://github.com/thepanlab/supercomputers)

### **Computer servers**

- **Thunder GPU server** (Dec. 2020)  
  For interactive deep learning on two RTX 3090 GPUs.    
  URL: thunder.cs.nor.ou.edu (SSH in OU intranet).  
  CPUs: AMD Ryzen Threadripper 3960X, 24 cores   
  GPUs: dual RTX 3090 24 GB.  
  RAM: 128 GB.  
  Disk: dual 2TB GB SSD.  
  [How to use Thunder](https://github.com/thepanlab/supercomputers/blob/master/thunder/thunder_tensorflow_gpu_conda.md).  

- **Laker GPU server** (May. 2022)  
  For interactive deep learning on two RTX A6000 GPUs.    
  URL: laker.cs.nor.ou.edu (SSH in OU intranet).  
  CPUs: AMD Ryzen Threadripper Pro 3955WX, 16 cores, 3.9 GHz    
  GPUs: dual NVIDIA RTX A6000 48 GB with NVLink 
  RAM: 256 GB  
  Disk: 3.84 TB SSD (NVMe)  

- **Blazer GPU server** (Nov. 2022)  
  For interactive deep learning on two RTX A6000 GPUs.    
  URL: laker.cs.nor.ou.edu (SSH in OU intranet).  
  CPUs: AMD Ryzen Threadripper PRO 5965WX, 24 cores, 3.8 GHz   
  GPUs: dual NVIDIA RTX A6000 48 GB with NVLink 
  RAM: 512GB
  Disk: 2 TB M.2 NVMe PCIe 4.0 SSD + 8TB 7200RPM 256MB CACHE 3.5IN SATA HDD ( DATA )

- **Virtual machines** on the [OU cloud](https://www.ou.edu/oscer/resources/our_cloud)  
  [Booming web server](http://booming.oscer.ou.edu)  
  Milkyway database server



