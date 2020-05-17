# Introduction
This code repository includes all of the files which satisfy the requirements of the "Getting and Cleaning Data Course Project".

# Files
run_analysis.R - The R code which performs all clean-up work
CodeBook.md - Describes the variables, the data and clean-up work performed
README.md - This document explains the project, files, and how they work

# The run_analysis.R script 
This file unzips the ZIP data files, then proceeds to import the data files of interest into data frames and tidy the data as per the assignment.

The steps performed by the script are further described in more detail below.

Extracting the raw data files
The run_analysis.R script extracts the ZIP file containing all data files using unzip(), then the data folder is entered using setwd().

Importing the data
Importing is performed using read.table(). Column names are assigned with col.names. Further data tidying of column names is performed using gsub().

Processing the "features"
The "test" and "train" data "features" were imported and tidied as described above. Other than applying column names to the "features" variables and cleaning-up those names, and removing the variables which were not of interest (no means or standard deviations), no other transformations were performed. Therefore, the "wide" format was used, meaning that there is a column for every "feature" variable that is a mean or standard deviation and also that there is only one value for each variable in each row. This is one of the forms of tidy data acceptable for this assignment. The other is "narrow" format, which would list the features as values of a "signals" column or similar.

Processing the subjects and activites
The two "subject" and "activity" variables have been included in the tidy data sets, and can be further described as:

subject (integers, 1-30)
activity (6 string labels used as factors in R)
Activity labels are assigned using factor().

User-defined functions
All of these data tidying operations are performed within user-defined functions in order to reuse code and to aid organization and readability. These functions come before the "Main Routine" section and are well commented.

Combining the data sets
The 66 numerical variables of the "features" data set were combined with the "activites" labled as factors, and integer "subjects" data using cbind() to produce 68-variable "test" and "train" data sets.

The "test" and "train" data sets were further combined with rbind() to produce the 10299-row "tidy" data set. Finally, an aggregated "data_tidy" data set with 180 rows was produced using aggregate().

Result Data Sets
The resulting data sets are summarized as follows:

tidy
data_tidy
Where "tidy" is the 10299-row combined data set with cleaned-up column names and labels, and only the mean and standard deviation values from the "feature vector" data.

"data_tidy" is the aggregated data set, grouped by subject and activity, producing a 180-row data frame.

Both data sets have 68 columns.

"data_tidy" is exported as a text file, "data_tidy.txt" and is written to the "UCI HAR Dataset" folder.

This file can be imported and viewed with these commands:
