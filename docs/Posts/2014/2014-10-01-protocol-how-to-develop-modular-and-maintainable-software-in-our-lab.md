---
id: 585
title: How to develop modular and maintainable software in the Pan lab
date: 2014-10-01T21:01:00+00:00
author: Chongle Pan
layout: post
guid: https://www.omicsbio.org/?p=585
permalink: /2014/10/01/protocol-how-to-develop-modular-and-maintainable-software-in-our-lab/
categories:
  - Protocols
---
**Recommended Group Practices for Software Development**

&nbsp;

Our group should follow a Unix development philosophy (<http://en.wikipedia.org/wiki/Unix_philosophy>). The essence is that “develop programs that do one thing and do it well”, which provides a high degree of flexibility and modularity. These programs will then be stitched together in different ways to accomplish big things. To integrate programs written by different members, we need to define a common interface of our programs. It is also very important to maintain a high standard for our production code to achieve maintainability and reusability across different applications.

**Command-line user interface:**

The recommended command calling a program should follow the format:

ProgramName -w WorkingDirectory -c ConfigurationFile -i InputFile -o OutputFile -h PrintHelp

Standard options:

-w: working directory that contains input and output files and the configuration file. If not provided, the default value is the current directory. If the input files have a common extension name, the program should process all files with that extension name in the working directory.

-c: configuration file that contains all the parameters needed for the program. If not provided, the default value is ProgramName.cfg in the working directory

-i: provide input file(s) to the program. If multiple types of input files are needed, other options should be used, e.g. -f, -g, etc. If not provided, use default filenames (or find default file extension) in the working directory.

-o: output file from the program. If not provided, use a default filename or a filename modified from the input file. This option may not be needed if the default filenames are not expected to be changed most of the time.

-h: to print help information that explains all the options and expected input files. Call this when there is any unknown option or errors in user input.

It is recommended that:

  1. All the options should have good default values to start.
  2. All parameters should be provided in the configuration file, not in the options, to leave a record to reproduce the processing.
  3. The program can only print errors, warnings, and the progress of the program to the stdout. All the output results should be saved to output files.

**Configuration file format:**

All the parameters for the program should be provided in the configuration file with an extension name of cfg. The cfg file format is based on the ini format (<http://en.wikipedia.org/wiki/INI_file>)

[section1]

\# comment

parameter = value

Because the ini format is poorly defined, we will use the following rules for the cfg file format:

  1. All parameters should have long descriptive meaningful name
  2. All parameters should have a unique name within a section.
  3. The program does not care about the order of parameters in a section.
  4. The section name is within [&#8230;.]
  5. Comment lines begin with “#”.
  6. Every parameter should have a comment line that explains the parameter and provide the expected values for the parameter
  7. The first “=” in a line separates the parameter name and the value.
  8. The parameter name goes from the first character of a line to “=”. Strip away all white spaces before and after the parameter name, but leave in all the white space inside.
  9. The value goes from “=” to the end of the line. Strip away all white spaces before and after the value, but leave in all the white space inside
 10. Master key set starts with a common name, followed by {subKey}. eg. MasterKey{subKey} =

**Input and output files:**

When possible, we should use file formats that are widely accepted, such as FASTA, MS2, etc. Otherwise, our programs should use a tab-delimited table format for input and output files.

  1. The comment lines begins with “#”.
  2. It  is recommended to use comment lines to record run parameters (e.g. copy the entire cfg file), provide result summary statistics, and describe the meaning of the column names.
  3. Comment lines may appear anywhere in the file and should always be ignored by the program.
  4. Tabs are the delimiter between columns and should not be used anywhere else.
  5. The first non-comment line is always the column header that provides a unique meaningful name for every column
  6. All other non-comment lines contains data that have the same number of fields as the column header
  7. A field that contains multiple items should follow the format: {item1,item2}, which is enclosed in { and } and use commas as the delimiter.

A two-level table format may be used when the above simple table format is not sufficient. An example is a table with proteins containing peptides. Then the table should have first-level rows for proteins and second-level rows for peptides.

  1. All the lines for the first-level rows should begin with “+” following a tab
  2. All the lines for the second-level rows should begin with “*” following a tab
  3. The first non-comment line is always the column header for the first-level rows
  4. The second non-comment line is always the column header for the second-level rows
  5. All second-level rows following a set of first-level rows belong to those first-level rows.

Example:

+    Protein      Description

*    Peptide1     Score        Sequence

*    Peptide2     Score        Sequence

It is recommended that

  1. Do not assume the position of a column will be fixed. Columns may be added, removed, and moved in a output file when the upstream program is revised. However, the names of the columns will be unique and stable across revisions. So, the header line of an output file need to be parsed to determine the position of a column.
  2. The input files and output files from a program should have unique extension names as provided in the help.
  3. Output files should have the cfg file used in the run provided in the comment lines at the beginning of the file. This provides a convenient to document and reproduce the output file.
  4. Some summary statistics can also be provided at the end of the output file in comment lines.

**Software development:**

It is recommended to use C++ for computing-intensive tasks and Python for everything else. R can be used for statistical analysis. Other programming languages can be used for prototyping if a significant amount of development time can be saved.

  1. It is mandatory to use long meaningful names for all functions and variables. It is recommended to use at least two complete words in all variable and function names. The words in a name may be separated by underscores (e.g. meaningful_name) or camel case (e.g. MeaningfulName or sMeaningfulName if it’s a string, following the Hungarian style). Only the most obvious acronyms or abbreviated words can be used. Because all programming editors can perform auto-completion, there is no reason to shorten variable names to save typing time. Since we don’t define name spaces, long variable names will also minimize the chance of naming conflicts.

[http://en.wikipedia.org/wiki/Naming\_conventions\_%28programming%29](http://en.wikipedia.org/wiki/Naming_conventions_%28programming%29)

  1. It is mandatory to comment code extensively. All the class variables and functions should be commented in the class definition. In the implementation, any block of code longer than 10 lines should be commented. Comments can be brief, but should be clear and useful to understand “why” (the purpose of some code), not “how” (“how” can be derived from the code itself).
  2. It is recommended to use object-oriented programming in C++ and Python for any non-trivial program. Classes can be defined following the input and output tables, i.e. rows as a list of objects and fields as member variables.
  3. The code should be deposited to SVN or some other version control system.
  4. It is recommended to follow the standard Python coding style,  <http://www.python.org/dev/peps/pep-0008/>
  5. Recommend Python 2 or Python 3 ?

More existing third party software is compatible with Python 2 than Python 3 right now. So, let us work with Python 2. Ted’s current version of Python is 2.7.2.

  1. For indenting, please use spaces or tab. Code indented with a mixture of tabs and spaces should be converted to using spaces or tab exclusively.

&nbsp;

To avoid the most common causes of program crashes and memory leaks,

  1. When performing a division, always check if the denominator is a zero or not
  2. When referencing an element in an array, always check if the index of the element is out of bound or not.
  3. When using an array of pointers to objects in the heap, always manage the deletion of those objects in one place, preferably in the destructor.

&nbsp;