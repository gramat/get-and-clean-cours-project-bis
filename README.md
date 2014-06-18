####The repo get-and-clean-cours-project-bis contains

Getting & Cleaning Data course project files

Coursera.org Data Science Specialization

* **run_analysis.R**
		script to obtain tidy_data.txt from Human Activity Recognition Using Smartphones Dataset
* **tidy_data.txt**
		data set obtained from Human Activity Recognition Using Smartphones Dataset
* **CodeBook.md**
		description for tidy_data.txt data
* **README.md**
		this file

######run_analysis.R
######NEEDS:
The training and test data sets and some descripting files extracted from 

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

**Original Data files list:**

* X_train.txt
* subject_train.txt
* y_train.txt
* X_test.txt
* subject_test.txt
* y_test.txt
* activity_labels.txt
* features.txt

These files must be situated in work directory 
or in  UCI HAR Dataset directory 
or in the original subdirectories of UCI HAR Dataset


######DOES:

* Merges the training and the test sets to create one data set.
* Extracts only the measurements on the mean and standard deviation for each measurement. 
* Uses descriptive activity names to name the activities in the data set
* Appropriately labels the data set with descriptive activity names. 
* Creates a second, independent tidy data set with the average of each variable for each activity and each subject. 

##########Step by step:
**Script** 
* checks if a original data files is in UCI HAR Dataset folder 
* or in one's subfolder
* or just in work directory
* if some files do not exist - stops script execution
* else loads the data from subject_train.txt ("subject"), X_train.txt (main data set), y_train.txt ("activities") in train data set
* loads the data from subject_test.txt ("subject"), X_test.txt (main data set),  y_test.txt ("activities") in test data set
* combines them in one data set
* loads the names of activities from activity_labels.txt
* set activities data in data set as factor with activities names
* gets the labels for data set variables from features.txt
* transforms them a bit to avoid any symbols except letter, numbers and point
* extracts and combines variables estimating means and standard deviations of the mesurements
* creates tidy data set assigning the cells the average of each variable for each activity and each subject.
* save data in a file "tidy_data.txt"
