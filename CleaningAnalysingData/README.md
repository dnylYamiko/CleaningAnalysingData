The repo includes the following files and directories:
=======================================================
- ReadMe.md
- "data": This is the directory that contains the "UCI HAR Dataset" dataset(files listed below)
- "run_analysis.R": The .R script that is reading relevant .txt files from "./data/UCI HAR Dataset". There is documentation included to explain the different commands used.
- "SecondaryTidyData.txt": This is the tidy dataset created by the .R script.
- "CodeBook.md": This contain the markup script for the codebook. The code book describes the variables, the data, and any transformations or work that you performed to clean up the data
- "CodeBook.html": This an html document for the codebook, this was done using the knit2html()

How analysis was done:
======================
- There are three core variables:1 Main 2. Test 3. Train
- Main : activity_labels Inertial Signals Inertial Signals Test: features subject_test subject_train Train: features.info X_test X_train
- ‘features_info.txt’: Shows information about the variables used on the feature vector. 
- ‘features.txt’: List of all features. 
- ‘activity_labels.txt’: Links the class labels with their activity name. 
- ‘train/X_train.txt’: Training set. 
- ‘train/y_train.txt’: Training labels. 
- ‘test/X_test.txt’: Test set. 
- ‘test/y_test.txt’: Test labels

- Analysis would show that the data can be categorised into 4 segments:  training set, test set, features and activity labels
- Inertial Signal data is not required. Additionally, features and activity label are more for tagging and descriptive than data sets.
- Only relevant files in the ./data/UCI HAR Dataset/ are read by run_analysis.R script. For reading I used the read.table(), with the file path as a parameter.
- Only the train and test files were read, that it, x_train.txt,y_train.txt,subject_train.txt,x_test.txt,y_test.txt and subject_test.txt
- Feautures.txt and activity_labels.txt are also read to get the actual activities being recorded.
- variables activity and subject and names of the activities have been labelled using descriptive names.In this part, Names of features will labelled using descriptive variable names. Replacing using the gsub() function
- From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject

The dataset(./data/UCI HAR Dataset/) includes the following files:
==================================================================

- 'README.txt'

- 'features_info.txt': Shows information about the variables used on the feature vector.

- 'features.txt': List of all features.

- 'activity_labels.txt': Links the class labels with their activity name.

- 'train/X_train.txt': Training set.

- 'train/y_train.txt': Training labels.

- 'test/X_test.txt': Test set.

- 'test/y_test.txt': Test labels.

The following files are available for the train and test data. Their descriptions are equivalent. 

- 'train/subject_train.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30. 

- 'train/Inertial Signals/total_acc_x_train.txt': The acceleration signal from the smartphone accelerometer X axis in standard gravity units 'g'. Every row shows a 128 element vector. The same description applies for the 'total_acc_x_train.txt' and 'total_acc_z_train.txt' files for the Y and Z axis. 

- 'train/Inertial Signals/body_acc_x_train.txt': The body acceleration signal obtained by subtracting the gravity from the total acceleration. 

- 'train/Inertial Signals/body_gyro_x_train.txt': The angular velocity vector measured by the gyroscope for each window sample. The units are radians/second. 
