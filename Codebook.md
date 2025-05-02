## Summary

This is a codebook for the final project for Getting and Cleaning Data.

## Data source

<https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip>

## Full description of the data

<http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones>

## library needed

-   library(reshape2)
-   library(dplyr)

## Dataset

-   Files need to be combined to merge test and train files: 1)
    "train/X_train.txt", 2) "train/y_train.txt",
    3)"train/subject_train.txt", 4) "test/x_test.txt", 5)
    "test/y_test.txt" , 6) "test/subject_test.txt", 7) "features.txt"
-   number of observations in the dataframe: 10299
-   number of variables in the dataframe: 563
-   number of variables with mean and sd: 81
-   There are 6 level of activities with their mean and sd for each
    subject.

<!-- -->

    ## [1] standing           sitting            laying             walking           
    ## [5] walking_downstairs walking_upstairs  
    ## 6 Levels: walking walking_upstairs walking_downstairs sitting ... laying

## Creating tidy dataset

-   An independent tidy dataset was created with the average of each
    variable for each activity and each subject:
-   number of observations: 180
-   numbre of variables : 81

<!-- -->

    ##  [1] "subjectID"                       "activity"                       
    ##  [3] "tBodyAcc.mean...X"               "tBodyAcc.mean...Y"              
    ##  [5] "tBodyAcc.mean...Z"               "tBodyAcc.std...X"               
    ##  [7] "tBodyAcc.std...Y"                "tBodyAcc.std...Z"               
    ##  [9] "tGravityAcc.mean...X"            "tGravityAcc.mean...Y"           
    ## [11] "tGravityAcc.mean...Z"            "tGravityAcc.std...X"            
    ## [13] "tGravityAcc.std...Y"             "tGravityAcc.std...Z"            
    ## [15] "tBodyAccJerk.mean...X"           "tBodyAccJerk.mean...Y"          
    ## [17] "tBodyAccJerk.mean...Z"           "tBodyAccJerk.std...X"           
    ## [19] "tBodyAccJerk.std...Y"            "tBodyAccJerk.std...Z"           
    ## [21] "tBodyGyro.mean...X"              "tBodyGyro.mean...Y"             
    ## [23] "tBodyGyro.mean...Z"              "tBodyGyro.std...X"              
    ## [25] "tBodyGyro.std...Y"               "tBodyGyro.std...Z"              
    ## [27] "tBodyGyroJerk.mean...X"          "tBodyGyroJerk.mean...Y"         
    ## [29] "tBodyGyroJerk.mean...Z"          "tBodyGyroJerk.std...X"          
    ## [31] "tBodyGyroJerk.std...Y"           "tBodyGyroJerk.std...Z"          
    ## [33] "tBodyAccMag.mean.."              "tBodyAccMag.std.."              
    ## [35] "tGravityAccMag.mean.."           "tGravityAccMag.std.."           
    ## [37] "tBodyAccJerkMag.mean.."          "tBodyAccJerkMag.std.."          
    ## [39] "tBodyGyroMag.mean.."             "tBodyGyroMag.std.."             
    ## [41] "tBodyGyroJerkMag.mean.."         "tBodyGyroJerkMag.std.."         
    ## [43] "fBodyAcc.mean...X"               "fBodyAcc.mean...Y"              
    ## [45] "fBodyAcc.mean...Z"               "fBodyAcc.std...X"               
    ## [47] "fBodyAcc.std...Y"                "fBodyAcc.std...Z"               
    ## [49] "fBodyAcc.meanFreq...X"           "fBodyAcc.meanFreq...Y"          
    ## [51] "fBodyAcc.meanFreq...Z"           "fBodyAccJerk.mean...X"          
    ## [53] "fBodyAccJerk.mean...Y"           "fBodyAccJerk.mean...Z"          
    ## [55] "fBodyAccJerk.std...X"            "fBodyAccJerk.std...Y"           
    ## [57] "fBodyAccJerk.std...Z"            "fBodyAccJerk.meanFreq...X"      
    ## [59] "fBodyAccJerk.meanFreq...Y"       "fBodyAccJerk.meanFreq...Z"      
    ## [61] "fBodyGyro.mean...X"              "fBodyGyro.mean...Y"             
    ## [63] "fBodyGyro.mean...Z"              "fBodyGyro.std...X"              
    ## [65] "fBodyGyro.std...Y"               "fBodyGyro.std...Z"              
    ## [67] "fBodyGyro.meanFreq...X"          "fBodyGyro.meanFreq...Y"         
    ## [69] "fBodyGyro.meanFreq...Z"          "fBodyAccMag.mean.."             
    ## [71] "fBodyAccMag.std.."               "fBodyAccMag.meanFreq.."         
    ## [73] "fBodyBodyAccJerkMag.mean.."      "fBodyBodyAccJerkMag.std.."      
    ## [75] "fBodyBodyAccJerkMag.meanFreq.."  "fBodyBodyGyroMag.mean.."        
    ## [77] "fBodyBodyGyroMag.std.."          "fBodyBodyGyroMag.meanFreq.."    
    ## [79] "fBodyBodyGyroJerkMag.mean.."     "fBodyBodyGyroJerkMag.std.."     
    ## [81] "fBodyBodyGyroJerkMag.meanFreq.."
