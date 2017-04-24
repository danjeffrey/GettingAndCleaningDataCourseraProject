# GettingAndCleaningDataCourseraProject
### Dan Jeffrey


Step 1 - load the needed libraries: data.table, dplyr



# 1. Merges the training and the test sets to create one data set.
subject_test <- read.table("test/subject_test.txt")
x_test <- read.table("test/X_test.txt")
y_test <- read.table("test/y_test.txt")
test = data.table(subject=subject_test,y_test,x_test)
remove("x_test", "y_test", "subject_test")

subject_train <- read.table("train/subject_train.txt")
x_train <- read.table("train/X_train.txt")
y_train <- read.table("train/y_train.txt")
train = data.table(subject=subject_train,y_train,x_train)
remove("x_train", "y_train", "subject_train")

allData <- rbind(test, train)
remove("train", "test")

# 2. Extracts only the measurements on the mean and standard deviation 
# for each measurement.

features <- read.table("features.txt")
wantedFeatures <- grep("(mean|std)\\(", features$V2)

#  ... save the column names for later
wantedFeatureNames <- as.character(features$V2[wantedFeatures])

# move the features two columns to the right to make room for the subject and activity.code:
wantedFeatures <- wantedFeatures + 2

# The following line is need to avoid duplicate names.
# Duplicate names cause dplyr select() to fail.
names(allData) <- make.names(names(allData), unique = TRUE)

# Select the columns with mean and std in the name
paredData <- select(allData, c(1, 2, wantedFeatures))
remove("allData")

# 3. Uses descriptive activity names to name the activities in the data set
activityLabels <- read.table("activity_labels.txt")

# name the activity code columns to avoid errors in merge:
names(activityLabels) <- c("activity.code", "activity.name")
names(paredData)[2] <- "activity.code"
paredData2 <- merge(activityLabels, paredData, by = "activity.code")
remove("paredData")

# 4. Appropriately labels the data set with descriptive variable names.
#  ... rename the subject column: 
names(paredData2)[3] <- "subject"
#  ... rename the feature columns:
names(paredData2)[4:length(names(paredData2))] <- wantedFeatureNames

# 5. From the data set in step 4, creates a second, independent tidy data 
#    set with the average of each variable for each activity and each subject.

groups <- group_by(paredData2, activity.name, subject)
summary <- summarize_all(groups, mean)


