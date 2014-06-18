##tidy_data.txt codebook 
Getting & Cleaning Data Course Project Data Set

Coursera.org 

Data Science Specialization


#### Original Data:

Human Activity Recognition Using Smartphones Dataset

Version 1.0

**Data source:**

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

**Data info:**

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Jorge L. Reyes-Ortiz, Davide Anguita, Alessandro Ghio, Luca Oneto.

Smartlab - Non Linear Complex Systems Laboratory

DITEN - Università degli Studi di Genova.

Via Opera Pia 11A, I-16145, Genoa, Italy.

www.smartlab.ws

**Description:**

The features selected for original database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). 

These signals were used to estimate variables of the feature vector for each pattern: 
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

Original Data set was transformed by **run_analysis.R** script:

####Transformations:

* Merged the training and the test sets to create one data set.
* Extracted only the measurements on the mean and standard deviation for each measurement. 
* Used descriptive activity names to name the activities in the data set
* Labeled the data set with descriptive names 
* Meanings of the variables = the average of each variable for each activity and each subject. 

####Transformed Data:

68 variables

180 observations

All **variables** except "subject" and "activities" were selected as the ones involving **the means and standard deviations** of the same mesurements in original data set. 
Variables are the **average of each original variable** for each activity and each subject.

* **subject**:
		index of persons observed, integer, rank: 1-30
* **activity**:
		visual fixed activities of persons, factor, levels: "WALKING", "WALKING_UPSTAIRS", "WALKING_DOWNSTAIRS", "SITTING", "STANDING", LAYING" 
* **tBodyAcc.mean.X**:
		numeric, rank: -1 - 1
* **tBodyAcc.mean.Y**:
		numeric, rank: -1 - 1
* **tBodyAcc.mean.Z**:
		numeric, rank: -1 - 1
* **tBodyAcc.std.X**:
		numeric, rank: -1 - 1
* **tBodyAcc.std.Y**:
		numeric, rank: -1 - 1
* **tBodyAcc.std.Z**:
		numeric, rank: -1 - 1
* **tGravityAcc.mean.X**:
		numeric, rank: -1 - 1
* **tGravityAcc.mean.Y**:
		numeric, rank: -1 - 1
* **tGravityAcc.mean.Z**:
		numeric, rank: -1 - 1
* **tGravityAcc.std.X**:
		numeric, rank: -1 - 1
* **tGravityAcc.std.Y**:
		numeric, rank: -1 - 1
* **tGravityAcc.std.Z**:
		numeric, rank: -1 - 1
* **tBodyAccJerk.mean.X**:
		numeric, rank: -1 - 1
* **tBodyAccJerk.mean.Y**:
		numeric, rank: -1 - 1
* **tBodyAccJerk.mean.Z**:
		numeric, rank: -1 - 1
* **tBodyAccJerk.std.X**:
		numeric, rank: -1 - 1
* **tBodyAccJerk.std.Y**:
		numeric, rank: -1 - 1
* **tBodyAccJerk.std.Z**:
		numeric, rank: -1 - 1
* **tBodyGyro.mean.X**:
		numeric, rank: -1 - 1
* **tBodyGyro.mean.Y**:
		numeric, rank: -1 - 1
* **tBodyGyro.mean.Z**:
		numeric, rank: -1 - 1
* **tBodyGyro.std.X**:
		numeric, rank: -1 - 1
* **tBodyGyro.std.Y**:
		numeric, rank: -1 - 1
* **tBodyGyro.std.Z**:
		numeric, rank: -1 - 1
* **tBodyGyroJerk.mean.X**:
		numeric, rank: -1 - 1
* **tBodyGyroJerk.mean.Y**:
		numeric, rank: -1 - 1
* **tBodyGyroJerk.mean.Z**:
		numeric, rank: -1 - 1
* **tBodyGyroJerk.std.X**:
		numeric, rank: -1 - 1
* **tBodyGyroJerk.std.Y**:
		numeric, rank: -1 - 1
* **tBodyGyroJerk.std.Z**:
		numeric, rank: -1 - 1
* **tBodyAccMag.mean**:
		numeric, rank: -1 - 1
* **tBodyAccMag.std**:
		numeric, rank: -1 - 1
* **tGravityAccMag.mean**:
		numeric, rank: -1 - 1
* **tGravityAccMag.std**:
		numeric, rank: -1 - 1
* **tBodyAccJerkMag.mean**:
		numeric, rank: -1 - 1
* **tBodyAccJerkMag.std**:
		numeric, rank: -1 - 1
* **tBodyGyroMag.mean**:
		numeric, rank: -1 - 1
* **tBodyGyroMag.std**:
		numeric, rank: -1 - 1
* **tBodyGyroJerkMag.mean**:
		numeric, rank: -1 - 1
* **tBodyGyroJerkMag.std**:
		numeric, rank: -1 - 1
* **fBodyAcc.mean.X**:
		numeric, rank: -1 - 1
* **fBodyAcc.mean.Y**:
		numeric, rank: -1 - 1
* **fBodyAcc.mean.Z**:
		numeric, rank: -1 - 1
* **fBodyAcc.std.X**:
		numeric, rank: -1 - 1
* **fBodyAcc.std.Y**:
		numeric, rank: -1 - 1
* **fBodyAcc.std.Z**:
		numeric, rank: -1 - 1
* **fBodyAccJerk.mean.X**:
		numeric, rank: -1 - 1
* **fBodyAccJerk.mean.Y**:
		numeric, rank: -1 - 1
* **fBodyAccJerk.mean.Z**:
		numeric, rank: -1 - 1
* **fBodyAccJerk.std.X**:
		numeric, rank: -1 - 1
* **fBodyAccJerk.std.Y**:
		numeric, rank: -1 - 1
* **fBodyAccJerk.std.Z**:
		numeric, rank: -1 - 1
* **fBodyGyro.mean.X**:
		numeric, rank: -1 - 1
* **fBodyGyro.mean.Y**:
		numeric, rank: -1 - 1
* **fBodyGyro.mean.Z**:
		numeric, rank: -1 - 1
* **fBodyGyro.std.X**:
		numeric, rank: -1 - 1
* **fBodyGyro.std.Y**:
		numeric, rank: -1 - 1
* **fBodyGyro.std.Z**:
		numeric, rank: -1 - 1
* **fBodyAccMag.mean**:
		numeric, rank: -1 - 1
* **fBodyAccMag.std**:
		numeric, rank: -1 - 1
* **fBodyBodyAccJerkMag.mean**:
		numeric, rank: -1 - 1
* **fBodyBodyAccJerkMag.std**:
		numeric, rank: -1 - 1
* **fBodyBodyGyroMag.mean**:
		numeric, rank: -1 - 1
* **fBodyBodyGyroMag.std**:
		numeric, rank: -1 - 1
* **fBodyBodyGyroJerkMag.mean**:
		numeric, rank: -1 - 1
* **fBodyBodyGyroJerkMag.std**: 
		numeric, rank: -1 - 1
