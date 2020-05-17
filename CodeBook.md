Files in the original data set

The original data set contains these files:

UCI HAR Dataset/activity_labels.txt
UCI HAR Dataset/features.txt
UCI HAR Dataset/features_info.txt
UCI HAR Dataset/README.txt
UCI HAR Dataset/test/Inertial Signals/body_acc_x_test.txt
UCI HAR Dataset/test/Inertial Signals/body_acc_y_test.txt
UCI HAR Dataset/test/Inertial Signals/body_acc_z_test.txt
UCI HAR Dataset/test/Inertial Signals/body_gyro_x_test.txt
UCI HAR Dataset/test/Inertial Signals/body_gyro_y_test.txt
UCI HAR Dataset/test/Inertial Signals/body_gyro_z_test.txt
UCI HAR Dataset/test/Inertial Signals/total_acc_x_test.txt
UCI HAR Dataset/test/Inertial Signals/total_acc_y_test.txt
UCI HAR Dataset/test/Inertial Signals/total_acc_z_test.txt
UCI HAR Dataset/test/subject_test.txt
UCI HAR Dataset/test/X_test.txt
UCI HAR Dataset/test/y_test.txt
UCI HAR Dataset/tidy_means.txt
UCI HAR Dataset/train/Inertial Signals/body_acc_x_train.txt
UCI HAR Dataset/train/Inertial Signals/body_acc_y_train.txt
UCI HAR Dataset/train/Inertial Signals/body_acc_z_train.txt
UCI HAR Dataset/train/Inertial Signals/body_gyro_x_train.txt
UCI HAR Dataset/train/Inertial Signals/body_gyro_y_train.txt
UCI HAR Dataset/train/Inertial Signals/body_gyro_z_train.txt
UCI HAR Dataset/train/Inertial Signals/total_acc_x_train.txt
UCI HAR Dataset/train/Inertial Signals/total_acc_y_train.txt
UCI HAR Dataset/train/Inertial Signals/total_acc_z_train.txt
UCI HAR Dataset/train/subject_train.txt
UCI HAR Dataset/train/X_train.txt
UCI HAR Dataset/train/y_train.txt

The files consist of documentation and data files. The data files consist of some files containing labels and column (variable) names and other files containing data values. The data values consist of subject numbers (30), activity types (6), coded as the integers 1-6 (with corresponding text values stored separately), and sensor signals, from a 561-column "feature vector".

The data set is split betweem two folders, "test" and "train". According to the documentaion provided with the raw data set, this partition was made randomly. For this clean-up project, we will combine these into a single data set.

Processing
This data clean-up project requires that the "test" and "train" data set are combined into a single data set. Another requirement of this clean-up is to include "only the measurements on the mean and standard deviation for each measurement".

Since only 66 of these "features" contain the mean and standard deviation values we are interested in, the rest of the "features" were removed from the data set during processing.

Further, since the "Inertial Signals" files do not contain mean and standard deviation values, these files were ignored for this project.

Therefore, of the remaining raw files:

UCI HAR Dataset/activity_labels.txt
UCI HAR Dataset/features.txt
UCI HAR Dataset/features_info.txt
UCI HAR Dataset/README.txt
UCI HAR Dataset/test/subject_test.txt
UCI HAR Dataset/test/X_test.txt
UCI HAR Dataset/test/y_test.txt
UCI HAR Dataset/train/subject_train.txt
UCI HAR Dataset/train/X_train.txt
UCI HAR Dataset/train/y_train.txt
The data files are:

UCI HAR Dataset/test/subject_test.txt
UCI HAR Dataset/test/X_test.txt
UCI HAR Dataset/test/y_test.txt
UCI HAR Dataset/train/subject_train.txt
UCI HAR Dataset/train/X_train.txt
UCI HAR Dataset/train/y_train.txt
Where:

"test" and "train" are the folders containing the two partitions of the data
subject_test.txt and subject_train.txt are the files of subject numbers
X_test.txt and X_train.txt are the files of "feature vector" data
y_test.txt and y_train.txt are the files of activity codes (1-6).
All three "test" files used have 2947 lines. The "train" files have 7352 lines.

The label and column-heading (variable name) files are

UCI HAR Dataset/activity_labels.txt
UCI HAR Dataset/features.txt
Where:

activity_labels.txt are the six labels for the subject's activities
features.txt are the 561 variable names of the "feature vector"
And the documentation files are:

UCI HAR Dataset/features_info.txt
UCI HAR Dataset/README.txt
Where:

README.txt introduces and describes the higher-level properties of the files
features_info.txt describes in detail the "feature vector" data set
Processing the "feature vector"
The features_info.txt file decodes the variable names for the "features".
