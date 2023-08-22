# TAMS
Trajectory Analysis and Mining Software

Usage instructions:

Download TAMS_executable
Make it executable by executing the command 'chmod u+x TAMS_executable'
Make sure gawk is installed

Run TAMS_executable as follows:
./TAMS_executable output file parameter first_group nr_of_groups second_group nr_of_groups third_group nr_of_groups
        
Output          = 0=stdOut, 1=AgregateFile, 2=RawData, 3=Bruteforce
File            = the CSV data file
Parameter       = The column number of the pain intensity parameter to analyze
First group     = Column number of the first subgroup
Nr_of_groups    = The number of groups to divide the first subgroup in
Second group    = (Optional) Column number of the second subgroup
Nr_of_groups    = (Optional) The number of groups to divide the second subgroup in
Third group     = (Optional) Column number of the third subgroup
Nr_of_groups    = (Optional) The number of groups to divide the third subgroup in

Example: ./TAMS_executable 2 DATASET_Exercise.csv 30 8 2 7 4 27 4
