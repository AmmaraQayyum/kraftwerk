
Project Title: 	
Child Mind Institute, problematic internet usage	
	
Dataset Information:	
The data is divided into two sets:	
1: Demographical data composed into a csv file total 3960 instances and 82 features.	
2: Physical activity data gathered through accelerometer compiled into parquet file, has 996 instances while 13 features.	
Target variable: sii (severity index) 0:None, 1:Mild, 2:Moderate, 3:Severe	
All the features in the parquet file are numerical.	
Almost half of features in the csv file are categorical while the rest are numerical.	
	
	
Distribution of the features:	
Distribution of the target variable is imbalance with the the following proportions: None : 58.3%, Mild:27.6%, Moderate:13.8%, Severe:1.2%	
Distribution of the age feature is unimodal with a single peak around the age of approximately (10-12) years. There is a gradual decline in the frequency as the age increases.	
Distribution of Sex column shows an imbalanced proportion with the 62.7% Male vs 33.3% Females.	
Distribution of the BIA-BIA_Activity_Level_num le is unimodal with a single peak around moderate and light activity level. There is a gradual decline in the frequency the activity level becomes intense.	
Distribution of rest of the BIA features are non normal, rightly skewed and have significant outliers. Most importantly  they are tightly distributed near the median thus have low variance.	
Distribution of the mostly physical features are unimodal and have less outliers.	
Distribution of the all FCG features are not normally distributed, some features presents unimodal, skewed, and bimodal distribution.	
Distribution of the PCIAT_Total is bimodal and rightly skewed. 	
	
Correlation between the target variables and the rest of the features:	
Sii and BIA features: min -0.01 max 0.41	
Sii and FCG Features: min -0.2 max 0.35	
Sii and Physical Features: min -0.04 max 0.31	
Sii and PCIAT: min 0.37 max 0.90	
	
Among all, the PCIAT features have the strongest correlation  with the target variable.	
	
Implementation of Models:	
I implemented several models using different amount of data.	
	
First Model:	
The first model is performed by calculating the correlation matrix and use that correlation to discard the	
features below a certain threshold.	
Steps Performed: 1 : Transformed the data using one-hot-encoder. 2 : Merged the encoded data and the numerical features to compile a data frame. 3 : Calculated the correlation matrix with the target variable. 4 : Drop all the features that has either positive correlation less than 0.3 or -0.3. 5 : Drop all the nan or infinity values. 6 : Perform the multiple models.	
	
Second Model:	
The second model is performed after merging the data from parquet and csv files.	
Steps perfromed: 1 : Merge the data from parquet and csv files and created a dataframe. 2 : Check the null acount and drop the column if the count of null value is greater than 60% 3 : Drop all the columns with the season word in its name 4 : Change the data type of the follwonig features: BIA-BIA_Activity_Level_num PreInt_EduHx-computerinternet_hoursday 5 : Drop the outliers 6 : Impute the null values 7 : Drop the infinity values 8 : Train and filt the model 9 : Record the results	
	
Third Model:	
The third model is like the second model with the following two differences:	
    1 : Outliers are not dropped	
    2 : Data is scaled through standard scaler before training the model	
    	
Fourth Model:	
The model is trained using PCA componets. The merged dataframe is traing using only two PCA componets instead	
of keeping all the features. Still the accuracy score is satisfied.	
	
Fifth Model:	
The very last model implemented on both types of data and performed PCA and manual feature removal to	
reduce the dimension of the data.	
Steps Performed: 1 : Reduce the dimentionalty of the accelometer data to 3 features instead of 13. 2 : Merged the data from parquet and csv files. 3 : Removed the null values for the target column. 4 : Create the mapping for null values. 5 : Impute the missing values and encoded the fatures thorugh onehotencoder and standard scale implemented thorugh pipeline. 6 : Fit and train the model. 7 : Predict and visualize the accuracy socre.	
	

