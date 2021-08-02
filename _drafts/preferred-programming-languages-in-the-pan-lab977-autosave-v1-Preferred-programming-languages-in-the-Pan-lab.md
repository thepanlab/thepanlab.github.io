---
id: 979
title: Preferred programming languages in the Pan lab
date: 2017-09-30T20:20:05+00:00
author: omicsbio
layout: revision
guid: https://www.omicsbio.org/2017/09/30/977-autosave-v1/
permalink: /2017/09/30/977-autosave-v1/
---
There are many programming languages for software development. Every language probably has its unique advantages. But our lab needs to maintain a consistent code base for code sharing and long-term maintenance and a coherent lab knowledge base for programming skills. So, I generally recommend the three programming languages below to start a bioinformatics project.

### Python

This is our preferred language for scripting. It is great for data processing and rapid prototyping. There are many packages available for machine learning, cloud computing, text mining, etc. The Python coding style makes it easy to write readable codes. Perl used to be very popular in the Bioinformatics community, but I strongly discourage the use of Perl for scripting because of the difficulty of maintaining Perl codes.

### R

This is our preferred language for statistics. R has libraries for nearly all statistics analyses. For research, it is much better than any commercial statistics package, like SAS, S, JMP, etc. R is also great for making high-quality figures for manuscripts.

### C++

This is our preferred language for developing computing-intensive or memory-intensive algorithms. It provides OpenMP for multi-threading and MPI for multiprocessing. C++ allows us to get close to the metal (e.g. counting bytes for memory usage). I think C++ is an improvement over C in nearly all aspects and is still as efficiency. And C++ provides many useful data structures and features from STL. But I discourage any dependency on the bloated Boost library. Since C++ is standardized, I think it is the real cross-platform language, as there are many good compilers across different platforms from Windows to the stripped-down Linux on supercomputer nodes.