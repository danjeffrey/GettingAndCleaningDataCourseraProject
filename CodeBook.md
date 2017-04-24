# Data Description
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

## Codebook
| column name | units | description |
|-------------|-------|-------------|
| activity.name | none | descriptive name of the activity 
| subject | none | which lab subject performed the activity (values = 1-30)
| activity.code | none |code for the activity (values = 1-6) | 
| tBodyAcc-mean()-X | g | average of mean body linear acceleration on x-axis |
| tBodyAcc-mean()-Y | g | average of mean body linear acceleration on y-axis |
| tBodyAcc-mean()-Z | g | average of mean body linear acceleration on z-axis |
| tBodyAcc-std()-X | g |  average of std deviation of body linear acceleration on x-axis |
| tBodyAcc-std()-Z | g |  average of std deviation of body linear acceleration on z-axis |
| tBodyAcc-std()-Y | g |  average of std deviation of body linear acceleration on y-axis |
| tGravityAcc-mean()-X | g | average of mean gravity acceleration on x axis |
| tGravityAcc-mean()-Y | g | average of mean gravity acceleration on y axis |
| tGravityAcc-mean()-Z | g | average of mean gravity acceleration on z axis |
| tGravityAcc-std()-X | g | average of standard deviation for gravity acceleration on x axis |
| tGravityAcc-std()-Y | g | average of standard deviation for gravity acceleration on y axis |
| tGravityAcc-std()-Z      | g | average of standard deviation for gravity acceleration on z axis |
| tBodyAccJerk-mean()-X | g | average of mean for jerk body acceleration on x axis |
| tBodyAccJerk-mean()-Y | g | average of mean  for jerk body acceleration on y axis |
| tBodyAccJerk-mean()-Z | g | average of mean  for jerk body acceleration on z axis |
| tBodyAccJerk-std()-X | g |  average of standard deviation for jerk body acceleration on x axis |
| tBodyAccJerk-std()-Y | g |  average of standard deviation for jerk body acceleration on y axis |
| tBodyAccJerk-std()-Z | g |  average of standard deviation for jerk body acceleration on z axis |
| tBodyGyro-mean()-X | radians/second | average of mean for body gyro angular velocity on x axis |
| tBodyGyro-mean()-Y | radians/second | average of mean for body gyro angular velocity on y axis |
| tBodyGyro-mean()-Z | radians/second | average of mean for body gyro angular velocity on z axis |
| tBodyGyro-std()-X |  radians/second | average of standard deviation for body gyro angular velocity on x axis |
| tBodyGyro-std()-Y |  radians/second | average of standard deviation for body gyro angular velocity on y axis |
| tBodyGyro-std()-Z |  radians/second | average of standard deviation for body gyro angular velocity on z axis |
| tBodyGyroJerk-mean()-X | radians/second | average of mean for body gyro jerk angular velocity on x axis |
| tBodyGyroJerk-mean()-Y | radians/second | average of mean for body gyro jerk angular velocity on y axis |
| tBodyGyroJerk-mean()-Z | radians/second | average of mean for body gyro jerk angular velocity on z axis |
| tBodyGyroJerk-std()-X | radians/second | average of standard deviation for body gyro jerk angular velocity on x axis |
| tBodyGyroJerk-std()-Y | radians/second | average of standard deviation for body gyro jerk angular velocity on y axis |
| tBodyGyroJerk-std()-Z | radians/second | average of standard deviation for body gyro jerk angular velocity on z axis |
| tBodyAccMag-mean() | g |     average of mean magnitude of 3D body acceleration signals |
| tBodyAccMag-std() | g  |     average of standard deviation of magnitude of 3D body acceleration signals |
| tGravityAccMag-mean() | g |  average of mean magnitude of 3D gravity acceleration signals | 
| tGravityAccMag-std() | g |   average of standard deviation of magnitude of 3D gravity acceleration signals |
| tBodyAccJerkMag-mean() | g | average of mean magnitude of 3D jerk acceleration signals |
| tBodyAccJerkMag-std() | g |  average of standard deviation of magnitude of 3D jerk acceleration signals |
| tBodyGyroMag-mean() | radians/second | average of mean magnitude of 3D body angular velocity |
| tBodyGyroMag-std() | radians/second |  average of standard deviation of magnitude of 3D body angular velocity |
| tBodyGyroJerkMag-mean() | radians/second |  average of mean magnitude of 3D jerk angular velocity |
| tBodyGyroJerkMag-std() | radians/second |   average of standard deviation of magnitude of 3D jerk angular velocity |
| fBodyAcc-mean()-X | g |  average of mean FFT of body linear acceleration on x-axis |
| fBodyAcc-mean()-Y | g |  average of mean FFT of body linear acceleration on y-axis | 
| fBodyAcc-mean()-Z | g |  average of mean FFT of body linear acceleration on z-axis |
| fBodyAcc-std()-X | g |   average of std deviation of FFT of body linear acceleration on x-axis |
| fBodyAcc-std()-Y | g |   average of std deviation of FFT of body linear acceleration on z-axis |
| fBodyAcc-std()-Z | g |   average of std deviation of FFT of body linear acceleration on y-axis |
| fBodyAccJerk-mean()-X | g | average of mean FFT for jerk body acceleration on x axis |
| fBodyAccJerk-mean()-Y | g | average of mean FFT for jerk body acceleration on y axis |
| fBodyAccJerk-mean()-Z | g | average of mean FFT for jerk body acceleration on z axis |
| fBodyAccJerk-std()-X | g |  average of standard deviation of FFT for jerk body acceleration on x axis |
| fBodyAccJerk-std()-Y | g |  average of standard deviation of FFT for jerk body acceleration on y axis |
| fBodyAccJerk-std()-Z | g |  average of standard deviation of FFT for jerk body acceleration on z axis |
| fBodyGyro-mean()-X | radians/second | average of mean FFT for body gyro angular velocity on x axis |
| fBodyGyro-mean()-Y | radians/second | average of mean FFT for body gyro angular velocity on y axis |
| fBodyGyro-mean()-Z | radians/second | average of mean FFT for body gyro angular velocity on z axis |
| fBodyGyro-std()-X | radians/second |  average of standard deviation of FFT for body gyro angular velocity on x axis |
| fBodyGyro-std()-Y | radians/second |  average of standard deviation of FFT for body gyro angular velocity on y axis |
| fBodyGyro-std()-Z | radians/second |  average of standard deviation of FFT for body gyro angular velocity on z axis |
| fBodyAccMag-mean() | g |                   average of mean FFT of magnitude of 3D body acceleration signals |
| fBodyAccMag-std()  | g |                   average of standard deviation of FFT of magnitude of 3D body acceleration signals |
| fBodyBodyAccJerkMag-mean() | g |           average of mean magnitude of FFT of 3D gravity acceleration signals | 
| fBodyBodyAccJerkMag-std() | g |            average of standard deviation of FFT of magnitude of 3D gravity acceleration signals |
| fBodyBodyGyroMag-mean() | radians/second | average of mean magnitude of FFT of 3D jerk acceleration signals |
| fBodyBodyGyroMag-std() | radians/second |  average of standard deviation of FFT of magnitude of 3D jerk acceleration signals |
| fBodyBodyGyroJerkMag-mean() | radians/second | average of mean magnitude of FFT of 3D jerk acceleration signals |
| fBodyBodyGyroJerkMag-std() | radians/second | average of standard deviation of FFT of magnitude of 3D jerk acceleration signals |





