# TAMS
Trajectory Analysis and Mining Software

# System Requirements
## Hardware requirements
`TAMS` package requires only a standard computer with enough RAM to support the in-memory operations.

## Software requirements
### OS Requirements
This package is supported for *macOS* and *Linux*. The package has been tested on the following systems:
+ macOS: Monterey (12.5)
+ Linux: Ubuntu 16.04

# Installation Guide:
### Install [gawk](https://www.gnu.org/software/gawk/)

- `brew install gawk`

Usage instructions:

- Download TAMS_executable
- Make it executable by executing the command
- `chmod u+x TAMS_executable`
- Create a directory named 'RESULTS' in the directory where the file 'TAMS_executable' is stored:
- `mkdir RESULTS`


# Run TAMS_executable as follows:
./TAMS_executable output file parameter first_group nr_of_groups second_group nr_of_groups third_group nr_of_groups
        
- Output          = 0=stdOut, 1=AgregateFile, 2=RawData, 3=Bruteforce
- File            = the CSV data file
- Parameter       = The column number of the pain intensity parameter to analyze
- First group     = Column number of the first subgroup
- Nr_of_groups    = The number of groups to divide the first subgroup in
- Second group    = (Optional) Column number of the second subgroup
- Nr_of_groups    = (Optional) The number of groups to divide the second subgroup in
- Third group     = (Optional) Column number of the third subgroup
- Nr_of_groups    = (Optional) The number of groups to divide the third subgroup in

Example: 
`./TAMS_executable 0 Example_dataset.csv 6 4 2`

# Expected output from the Example dataset:
```
Dataset = Example_dataset
Parameter name = PainIntensity
Number of subjects = 20
Number of measurements = 1014
Number of studies = 1
Name of studies = Example_dataset
 
Sex     Participants   	Follow-Ups     	Persistent     	Progressing    	Rapidly    Gradually	SingleEpisodic 	Episodic    Fluctuating    
Male          9	             448	     1	             1	           1	       2	       1	    2	        1
Female       11	             566	     1	             1	           1	       1	       1	    3	        3
Totals       20	            1014	     2	             2	           2	       3	       2	    5	        4

Number of classified patients: 20
Number of rest patients: 
```

# Expected runtime:
0.11 seconds

# License

This project is covered under the **GNU 3.0 License**.
