#Introduction
The script "run_analysis.R" can be perform the 5 steps described in the course project's getting and cleaning data.

Steps:
All the similar data is merged using the rbind() function. similarly, we take the files having the same number of columns and referring to the same entities. in this way, only those columns with the mean and standard deviation measures are taken from the dataset. 

After extracting the columns, it is given your correct names, taken from the  "features.txt" file.

The data of  "activity" is addressed with values 1 to 6, take the activity names and IDs from "activity_labels.txt" files, it is substituted in the dataset.

In the dataset, the columns with vague column names are corrected.

Ultimately, it is generated a new dataset with all average measures for each subject and activity type (30 subjects * 6 activities). The last file created  is called averages_data.txt, and uploaded to this repository.

#Variables<p>
<b>contain the data from the downloaded files:</b><p>
1) y_train;<p>
2) x_train;<p>
3) y_test;<p>
4) x_test;<p>
5) subject_test;<p>
6) subject_train.<p>

<b>Subject_data merge the previous datasets to further analysis:</b><p>
1) x_data;<p>
2) y_data.<p>


<b>x_data</b><p>
The correct names for the x_data dataset is in "features" (stored in mean_and_std_features) that was applied to the column names , a vector used to extract the filtered data.
A similar approach is taken with activity names through the activities variable.


<b>all_data</b><p>
The big dataset all_data, merges: x_data, y_data and subject_data.
From the plyr package, "ddply()",  is used to be aplicate "colMeans()" and ease the development of the project.
In the end, the "averages_data" have the averages which will be later stored in a text file. 
