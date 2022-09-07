# UMD-alumni-data-analysis
[Objective]
Our ultimate goal is to help the association increase the number of first-time attendees and major prospects, which is the person who can donate more than 50,000 dollars. We set these two columns as our target variables and use other variables in the dataset to figure out feasible improvements.
Reorganize data structure 
We cleaned and reorganized the data source for our further analysis.
1.	concatenate all sheets into one dataframe from the excel file
2.	add the weekend column using the calendar library
3.	Separate the event date and group description to smaller groups. 
4.	Use the label encoder function to transfer the categorical data into the numerical data. 
 As a result, we have 22 columns in total. 
Grouping 
We group by four variables - activity code, location code, group code, and month to find the relationship between these variables and the mean of participation, major prospects percentage, and first-time attendees percentage.
We also took a deep look into the time, turning the date into the weekdays and weekends, then we found that events held on weekdays tend to be more attractive among the targeted groups.
 
Therefore, we can take all these variables into consideration to hold a better event to achieve our goal.
Prediction is the second half of our project where we are trying to predict major prospects and first time attendees for upcoming events. 

We have used Gaussian and Kernel Regression for prediction.Since these regression techniques are non-parametric, it allows a flexible number of parameters as the sample size increases. It provides us the scope of expansion in the future where we can incorporate attributes that are highly correlated with major prospects and first time attendees' value. 

For now, we have used participation, location code, group code and activity code in order to predict major prospects' value. Since location code, group code and activity code were categorical variables, we first converted them into numerical variables using encoding. We then split data into train and test. For validation, if the corresponding value of Major Prospects in the database for above codes and participation value was 6, our model could predict it as 5.98. We get a Mean squared error = 142. In future, we plan to apply various regression techniques and choose the technique which provides better statistical results.

For prediction, we asked for user inputs and our model could predict the percentage major prospects for given inputs.
Similarly, we have tried to predict the first time attendees value using Gaussian and kernel regression. 

For validation, if the corresponding value of First Time Attendees in the database for above codes and participation value was 10, our model could predict it as 9.84. We get a Mean squared error = 1136. In future, we plan to apply various regression techniques and choose the technique which provides better statistical results.

For prediction, we asked for user inputs and our model could predict the percentage first-time attendees for the given inputs.
Conclusion

Based on our previous analysis, our team comes up with some recommendations on several facets to achieve our future objectives.
On Time-wise, the Alumni Association should hold events/ more often on three important time periods that are Weekdays and Summertime to get more participation and major prospects.
 and From August to October, which is the beginning of the Fall semester /to attract more first-time attendees

On the Location-wise on-campus social events will be a good idea. 

On Activity-wise, the association should plan more appealing online events to avoid the negative impact of COVID.
 
Lastly on the Group-wise, Focus on Stewardship and Membership for higher donation
Future work
●	Add more data like “Event Duration” or “Alumni Salary or Profession” to do more analysis and gain insights.
●	Implement other regression techniques and find attributes that are highly correlated with first-time attendees and major prospects in order to increase the prediction accuracy of the model.
●	Apply in-depth statistical analysis to better understand the correlation between the attributes.
