# Code Book
## Dan Jeffrey's Homework for Coursera 

The features selected for this database come from the accelerometer and gyroscope 
3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' 
to denote time) were captured at a constant rate of 50 Hz. Then they were filtered 
using a median filter and a 3rd order low pass Butterworth filter with a corner 
frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then 
separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) 
using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

Subsequently, the body linear acceleration and angular velocity were derived in time 
to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude 
of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, 
tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing 
fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, 
fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). 

These signals were used to estimate variables of the feature vector for each pattern:  
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.
* tBodyAcc-XYZ        
* tGravityAcc-XYZ       
* tBodyAccJerk-XYZ
* tBodyGyro-XYZ
* tBodyGyroJerk-XYZ
* tBodyAccMag
* tGravityAccMag
* tBodyAccJerkMag
* tBodyGyroMag
* tBodyGyroJerkMag
* fBodyAcc-XYZ
* fBodyAccJerk-XYZ
* fBodyGyro-XYZ
* fBodyAccMag
* fBodyAccJerkMag
* fBodyGyroMag
* fBodyGyroJerkMag
 
The set of variables that were estimated from these signals are: 
 
* mean(): Mean value
* std(): Standard deviation
* meanFreq(): Weighted average of the frequency components to obtain a mean 
 
Additional vectors obtained by averaging the signals in a signal window sample. These are used on the angle() variable:
* gravityMean
* tBodyAccMean
* tBodyAccJerkMean
* tBodyGyroMean
* tBodyGyroJerkMean

The fields are means of all of the values in the original raw 
data -- calculated for each activity/subject pair:

| column name | units | description |
|-------------|-------|-------------|
| activity.name | none | descriptive name of the activity 
| subject | none | which lab subject performed the activity (values = 1-30)
| activity.code | none |code for the activity (values = 1-6) | 
| tBodyAcc-mean()-X | g | |
| tBodyAcc-mean()-Y | g | |
| tBodyAcc-mean()-Z | g | |
| tBodyAcc-std()-X | g | |
| tBodyAcc-std()-Y | g | |
| tBodyAcc-std()-Z | g | |
| tGravityAcc-mean()-X | g | |
| tGravityAcc-mean()-Y | g | |
| tGravityAcc-mean()-Z | g | |
| tGravityAcc-std()-X | g | |
| tGravityAcc-std()-Y | g | |
| tGravityAcc-std()-Z      | g | |
| tBodyAccJerk-mean()-X | g | |
| tBodyAccJerk-mean()-Y | g | |
| tBodyAccJerk-mean()-Z | g | |
| tBodyAccJerk-std()-X | g | |
| tBodyAccJerk-std()-Y | g | |
| tBodyAccJerk-std()-Z | g | |
| tBodyGyro-mean()-X | radians/second | |
| tBodyGyro-mean()-Y | radians/second | |
| tBodyGyro-mean()-Z | radians/second | |
| tBodyGyro-std()-X | radians/second | |
| tBodyGyro-std()-Y | radians/second | |
| tBodyGyro-std()-Z | radians/second | |
| tBodyGyroJerk-mean()-X | radians/second | |
| tBodyGyroJerk-mean()-Y | radians/second | |
| tBodyGyroJerk-mean()-Z | radians/second | |
| tBodyGyroJerk-std()-X | radians/second | |
| tBodyGyroJerk-std()-Y | radians/second | |
| tBodyGyroJerk-std()-Z | radians/second | |
| tBodyAccMag-mean() | g | |
| tBodyAccMag-std() | g | |
| tGravityAccMag-mean() | g | |
| tGravityAccMag-std() | g | |
| tBodyAccJerkMag-mean() | g | |
| tBodyAccJerkMag-std() | g | |
| tBodyGyroMag-mean() | radians/second | |
| tBodyGyroMag-std() | radians/second | |
| tBodyGyroJerkMag-mean() | radians/second | |
| tBodyGyroJerkMag-std() | radians/second | |
| fBodyAcc-mean()-X | g | |
| fBodyAcc-mean()-Y | g | | 
| fBodyAcc-mean()-Z | g | |
| fBodyAcc-std()-X | g | |
| fBodyAcc-std()-Y | g | |
| fBodyAcc-std()-Z | g | |
| fBodyAccJerk-mean()-X | g | |
| fBodyAccJerk-mean()-Y | g | |
| fBodyAccJerk-mean()-Z | g | |
| fBodyAccJerk-std()-X | g | |
| fBodyAccJerk-std()-Y | g | |
| fBodyAccJerk-std()-Z | g | |
| fBodyGyro-mean()-X | radians/second | |
| fBodyGyro-mean()-Y | radians/second | |
| fBodyGyro-mean()-Z | radians/second | |
| fBodyGyro-std()-X | radians/second | |
| fBodyGyro-std()-Y | radians/second | |
| fBodyGyro-std()-Z | radians/second | |
| fBodyAccMag-mean() | g | |
| fBodyAccMag-std()  | g | |
| fBodyBodyAccJerkMag-mean() | g | |
| fBodyBodyAccJerkMag-std() | g | |
| fBodyBodyGyroMag-mean() | radians/second | |
| fBodyBodyGyroMag-std() | radians/second | |
| fBodyBodyGyroJerkMag-mean() | radians/second | |
| fBodyBodyGyroJerkMag-std() | radians/second | |





