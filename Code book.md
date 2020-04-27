---
title: "Code Book"
author: "Jun N"
date: "4/26/2020"
output: pdf_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

## R Markdown
Files:
Original dataset: UCI HAR dataset 
Finaldata: final clean data
Run_analysis.R script:  is run to prepare the data and then get the clean data upon the five steps required in the project.
Strategies: 
1.	Generate work directory and check if potential packages available
2.	Create folders under work directory
3.	Create new repo in Github with README.MD(describe purpose and goal of the project)
4.	Create new project in R studio with version control (Git)
5.	Download the dataset:  UCI HAR Dataset
6.	Write and edit and run R script
7.	Assign variables 
	features <- features.txt 
	activities <- activity_labels.txt 
	subject_test <- test/subject_test.txt 
	x_test <- test/X_test
	y_test <- test/y_test.txt 
	subject_train <- test/subject_train.txt 
	x_train <- test/X_train.txt 
	y_train <- test/y_train.txt
8.	Merges the training and the test sets to create one data set
•	X: by merging x_train and x_test using rbind() function
•	Y: by merging y_train and y_test using rbind() function
•	Subject: by merging subject_train and subject_test using rbind() function
•	Merged_Data: merging Subject, Y and X using cbind() function
9.	Extracts only the measurements on the mean and standard deviation for each measurement
•	TidyData: subsetting Merged_Data, 
•	columns: subject, code and the measurements on the mean and standard deviation (std) for each measurement
10.	Uses descriptive activity names to name the activities in the data set
11.	Appropriately labels the data set with descriptive variable names
•	code column: activities
•	Acc: Accelerometer
•	Gyro: Gyroscope
•	BodyBody: Body
•	Mag: Magnitude
•	Start with character f: Frequency
•	Start with character t: Time
12.	From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject
o	FinalData is first grouped by subject and activity and then created by summarizing TidyData by taking means of each variable for each activity/subject.



```{r cars}
See attached R script in Github
```


