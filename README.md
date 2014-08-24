gettingdata-project
===================

It is getting and cleaning data course project on coursera.
We are provided with the data UCI HAR dataset to read and produce a tidy dataset out of it.


The working of the run_analysis.R script can be described in following steps:-

The dataset is downloaded manually. Thus data is stored in a folder UCI HAR Dataset after extraction.
The working directory in R is set to the folder location and all processing is done inside that working directory.

1. Reading of data as a data.frame 
   The first part of code describes the reading of all the required text files from the dataset namely features.txt,
   activity_labels.txt, /train/subject_train.txt, /train/X_train.txt, /train/y_train.txt,/test/subject_test.txt, /test/X_test.txt
   and /test/subject_test.txt

2. Setting the column name of the dataframes to a meaningful one to make the data more human readable and understandable.

3. Fitting the data together after examining their height and width. The data are combined with the help of cbind(). Using the cbind()
   function first of all we created a training dataset combining the dataframe namely subjectTrain, xTrain, yTrain. Similarly test dataset
   is generated combining the dataframe namely subjectTest, xTest, yTest. Finally a big dataset named as finalData is generated by 
   row binding the two datasets trainingData and testData.

4. As the finalData set contain all the features, we need to subset the data frame to get only mean and standard deviation values.
   Thus all the column names containing mean(mean()) and standard deviation(std()) are extracted out using pattern searching grep command.
   The selected column is stored in a separate vector "colvector". 

5. The subsetting of finalData is done using colvector and thus a dataset with lesser number of column. It contains only the relevant mean()
   and std() column names.

6. In this step, the column names of the finalData set generated are replaced with the meaningful one. Again pattern searching and replacement 
   technique is used inside the loop.

7. The newly created column names i.e. the descriptive name of the finalData is assigned to the finalData. It creates finalData set 
   with descriptive and meaningful column name.

8. The descriptive dataset is now aggregated so as to get the average values for each subject for each activity. This generates two columns
   that are duplicated in the dataset. After proper subsetting of the dataframe i.e. removing the duplicates columns from the data, we are 
   having a final data set which can be called as tidydata.

9. The tidyData is written to a text file using write.table() with row.names=FALSE. Thus a tidy dataset is exported to a text 
   file tidydata1.txt.

10. A tidy data is generated into a text file.
   
