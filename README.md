# GettingAndCleaningDataCourseraProject
### Dan Jeffrey

## Other documents:
* [Code book](https://github.com/danjeffrey/GettingAndCleaningDataCourseraProject/blob/master/CodeBook.md)
* [R script](https://github.com/danjeffrey/GettingAndCleaningDataCourseraProject/blob/master/run_analysis.R):

## Steps performed by the script, [run_Analysis.R](https://github.com/danjeffrey/GettingAndCleaningDataCourseraProject/blob/master/run_analysis.R):

First, load the needed libraries: data.table, dplyr

1. Merges the training and the test sets to create one data set.
	a. Read subject_test, x_test, and y_test
	b. Combine tables from step 1.a into a single table named, test
	c. Read subject_train, x_train, and y_train
	d. combine tables from step 1.c into a single table named, train
	e. Combine all rows from test and train into one table named allData

2. Extracts only the measurements on the mean and standard deviation for each measurement.
	a. Read features.txt 
	b. Find all of the fields in features.txt that contain "mean" or std" -- save as a list of indexes
		NOTE: I included everything here. Instructions were not explicit about getting everything or just the ones ending in std(0 or mean() 
	c. Save the wanted column names for later
	d. Move the features two columns to the right to make room for the subject and activity.code from the other tables loaded above
	e. Duplicate names cause dplyr select() to fail. So use make.names to avoid that
	f. Select the columns form allData that we want to keep using the indexes found in step 2.b
		This is named paredData
	
3. Uses descriptive activity names to name the activities in the data set
	a. Read the activity_labels.txt file to get activity names
	b. Rename the activity code columns to avoid errors in merge below
	c. Merge the activity labels table into the paredData table -- and call it paredData2

4. Appropriately labels the data set with descriptive variable names.
	a. Rename the subject column to "subject"
	b. Rename the feature columns using the saved names from step 2c above

5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
	a. Group the table on activity and subject and name it groups
	b. Call summarize_all on groups to get the mean of each column.
	c. Save it as summary

6. Write the final output to todySummary.txt

	





