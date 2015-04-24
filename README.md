# Coursera Getting-and-Cleaning Data Project

Josh Freeman

## Description 

  This document is to give additional information (variables, data, and transformations) used in the Johns Hopkins MOOC "Getting and Cleaning Data Course" on Coursera. 

##Source
    [Data Description](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)
    [Data Source File](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)
    
## Data Set Information
A group of 30 volunteers, in the age range of 19-48, performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) while wearing a smartphone (Samsung Galaxy S II) on the waist. The galaxy's accelerometer and gyroscope were utilized at a constant rate of 50Hz to capture the 3-axial linear acceleration and 3-axial angular velocity. The group was video-recorded to label the data manually. The dataset was partitioned randomly into two sets with 70% of the group's data used for the training data and the test data using the remaining 30%. 

The noise filtering and sampling (in a fixed-width windows of 2.56sec and 50% overlap, 128 readings/window) were used on the sensor signals. Butterworth low-pass filter was used on the acceleration signal to seperate the body acceleration and gravity. The gravitational force is assumed to have only low frequency components, so a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.

## Attribute Information
For each record in the dataset it is provided: 
- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration. 
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.

## Section 1. Merge the training and the test sets to create one data set.
After setting the source directory for the files, read into tables the data located in
- features.txt
- activity_labels.txt
- subject_train.txt
- x_train.txt
- y_train.txt
- subject_test.txt
- x_test.txt
- y_test.txt

Assign column names and merge to create one data set.

## Section 2. Extract only the measurements on the mean and standard deviation for each measurement. 
Create a logcal vector that contains TRUE values for the ID, mean and stdev columns and FALSE values for the others.
Subset this data to keep only the necessary columns.

## Section 3. Use descriptive activity names to name the activities in the data set
Merge data subset with the activityType table to cinlude the descriptive activity names

## Section 4. Appropriately label the data set with descriptive activity names.
Use gsub function for pattern replacement to clean up the data labels.

## Section 5. Create a second, independent tidy data set with the average of each variable for each activity and each subject. 
Per the project instructions, we need to produce only a data set with the average of each veriable for each activity and subject

