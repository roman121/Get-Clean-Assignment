# Get-Clean-Assignment
"run_analysis.R" is the script that
1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement.
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive activity names.
5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.
Please go through that script. I've commented and described every sections clearly. I'll also go through briefly in this section

You're working directory should contain "UCI HAR Dataset" directory. data.table and reshape2 package will be installed if it is not 
installed previously. This section checks if it is installed, if not it install data.table package. Same is for reshape2.
    if (!require("data.table"))
    {
      install.packages("data.table")
    }
  
  #for test data --  
 activity file,features is loaded  to get activity labels and features. Extract  mean and standard deviation features with grepl.
 assign every data of X_test with column name from features. Extract  mean and standard deviation column names . assign column name and then bind data.
 
 #Same process is for train data
 
 Finally, Merges the training and the test sets to create one data set and Create independent tidy data set with the average of each variable for each activity and each subject.

