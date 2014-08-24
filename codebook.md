				Data Dictionary- tidydata1 (Human Activity Recognition)
 	Activity
		code
		1 WALKING
		2 WALKING_UPSTAIRS
		3 WALKING_DOWNSTAIRS
		4 SITTING
		5 STANDING
		6 LAYING
    
        subjectID
		It identifies the subject who performed the activity for each window sample. Its range is from 1 to 30. There are 30 subjects.
		Each subjectId either starts with time or freq stands for time domain and frequency domain respectively.
		Each subjectID end with either Mean or StdDev stands for the mean and standard deviation for the body activity.
                Other things like Acc and Jerk stands for Acceleration and jerk of certain magnitude.
		The value recorded by the gyroscope were also recorded and their means and standard deviations are calculated to those subjectID
		that contains Gyro in their names.

		These are the signals recorded so they are in Hz units.
		The IDs are as follows:-

	timeBodyAccMagnitudeMean
        timeGravityAccMagnitudeMean
    	timeBodyAccJerkMagnitudeMean
	timeBodyGyroMagnitudeMean
  	timeBodyGyroJerkMagnitudeMean 
	freqBodyAccMagnitudeMean 
  	freqBodyAccJerkMagnitudeMean 
	freqBodyGyroMagnitudeMean
	freqBodyGyroJerkMagnitudeMean
	timeBodyAccMagnitudeStdDev 
	timeGravityAccMagnitudeStdDev
	timeBodyAccJerkMagnitudeStdDev 
	timeBodyGyroMagnitudeStdDev
	timeBodyGyroJerkMagnitudeStdDev
	freqBodyAccMagnitudeStdDev
	freqBodyAccJerkMagnitudeStdDev 
	freqBodyGyroMagnitudeStdDev
	freqBodyGyroJerkMagnitudeStdDev 

