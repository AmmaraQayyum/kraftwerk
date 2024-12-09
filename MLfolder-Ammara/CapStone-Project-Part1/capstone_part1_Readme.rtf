{\rtf1\ansi\ansicpg1252\cocoartf2761
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fnil\fcharset0 HelveticaNeue-Bold;\f1\fnil\fcharset0 HelveticaNeue;\f2\fnil\fcharset0 HelveticaNeue-Italic;
\f3\fnil\fcharset0 HelveticaNeue-BoldItalic;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\deftab560
\pard\pardeftab560\sa40\partightenfactor0

\f0\b\fs32 \cf0 Project Title: \
\pard\pardeftab560\slleading20\partightenfactor0

\f1\b0\fs26 \cf0 Child Mind Institute, problematic internet usage\
\
\pard\pardeftab560\sa40\partightenfactor0

\f0\b\fs32 \cf0 Dataset Information:\
\pard\pardeftab560\slleading20\partightenfactor0

\f1\b0\fs26 \cf0 The data is divided into two sets:\
1: 
\f0\b Demographical
\f1\b0  data composed into a csv file total 
\f0\b 3960
\f1\b0  instances and 
\f0\b 82
\f1\b0  features.\
2: 
\f0\b Physical activity
\f1\b0  data gathered through accelerometer compiled into parquet file, has 
\f0\b 996
\f1\b0  instances while 
\f0\b 13 
\f1\b0 features.\
Target variable: 
\f0\b sii (severity index)
\f1\b0  0:
\f2\i None
\f1\i0 , 1:
\f2\i Mild
\f1\i0 , 2:
\f2\i Moderate
\f1\i0 , 3:
\f2\i Severe
\f1\i0 \
All the features in the parquet file are numerical.\
Almost half of features in the csv file are categorical while the rest are numerical.\
\
\
\pard\pardeftab560\sa40\partightenfactor0

\f0\b\fs32 \cf0 Distribution of the features:\
\pard\pardeftab560\slleading20\partightenfactor0

\f1\b0\fs26 \cf0 Distribution of the target variable is imbalance with the the following proportions: 
\f3\i\b None
\f1\i0\b0  : 58.3%, 
\f3\i\b Mild
\f1\i0\b0 :27.6%, 
\f3\i\b Moderate
\f1\i0\b0 :13.8%, 
\f3\i\b Severe
\f1\i0\b0 :1.2%\
Distribution of the age feature is unimodal with a single peak around the age of approximately (10-12) years. There is a gradual decline in the frequency as the age increases.\
Distribution of 
\f0\b Sex
\f1\b0  column shows an imbalanced proportion with the 62.7% 
\f0\b Male
\f1\b0  vs 33.3% 
\f0\b Females
\f1\b0 .\
Distribution of the 
\f0\b BIA-BIA_Activity_Level_num
\f1\b0  le is unimodal with a single peak around moderate and light activity level. There is a gradual decline in the frequency the activity level becomes intense.\
Distribution of rest of the BIA features are non normal, rightly skewed and have significant outliers. Most importantly  they are tightly distributed near the median thus have low variance.\
Distribution of the mostly physical features are unimodal and have less outliers.\
Distribution of the all FCG features are not normally distributed, some features presents unimodal, skewed, and bimodal distribution.\
Distribution of the PCIAT_Total is bimodal and rightly skewed. \
\pard\pardeftab560\slleading20\pardirnatural\partightenfactor0
\cf0 \
\pard\pardeftab560\sa40\partightenfactor0

\f0\b\fs32 \cf0 Correlation between the target variables and the rest of the features:\
\pard\pardeftab560\slleading20\partightenfactor0

\f1\b0\fs26 \cf0 Sii and BIA features: min -0.01 max 0.41\
Sii and FCG Features: min -0.2 max 0.35\
Sii and Physical Features: min -0.04 max 0.31\
Sii and PCIAT: min 0.37 max 0.90\
\pard\pardeftab560\slleading20\pardirnatural\partightenfactor0
\cf0 \
\pard\pardeftab560\slleading20\partightenfactor0

\f0\b \cf0 Among all, the PCIAT features have the strongest correlation  with the target variable.\
\pard\pardeftab560\slleading20\pardirnatural\partightenfactor0
\cf0 \
\pard\pardeftab560\sa40\partightenfactor0

\fs32 \cf0 Implementation of Models:\
\pard\pardeftab560\slleading20\partightenfactor0

\f1\b0\fs26 \cf0 I implemented several models using different amount of data.\
\
\pard\pardeftab560\slleading20\partightenfactor0

\f0\b \cf0 First Model:\
\pard\pardeftab560\slleading20\partightenfactor0

\f1\b0 \cf0 The first model is performed by calculating the correlation matrix and use that correlation to discard the\
features below a certain threshold.\
Steps Performed: 1 : Transformed the data using one-hot-encoder. 2 : Merged the encoded data and the numerical features to compile a data frame. 3 : Calculated the correlation matrix with the target variable. 4 : Drop all the features that has either positive correlation less than 0.3 or -0.3. 5 : Drop all the nan or infinity values. 6 : Perform the multiple models.\
\pard\pardeftab560\slleading20\pardirnatural\partightenfactor0
\cf0 \
\pard\pardeftab560\slleading20\partightenfactor0

\f0\b \cf0 Second Model:\
\pard\pardeftab560\slleading20\partightenfactor0

\f1\b0 \cf0 The second model is performed after merging the data from parquet and csv files.\
Steps perfromed: 1 : Merge the data from parquet and csv files and created a dataframe. 2 : Check the null acount and drop the column if the count of null value is greater than 60% 3 : Drop all the columns with the season word in its name 4 : Change the data type of the follwonig features: BIA-BIA_Activity_Level_num PreInt_EduHx-computerinternet_hoursday 5 : Drop the outliers 6 : Impute the null values 7 : Drop the infinity values 8 : Train and filt the model 9 : Record the results\
\pard\pardeftab560\slleading20\pardirnatural\partightenfactor0
\cf0 \
\pard\pardeftab560\slleading20\partightenfactor0

\f0\b \cf0 Third Model:\
\pard\pardeftab560\slleading20\partightenfactor0

\f1\b0 \cf0 The third model is like the second model with the following two differences:\
    1 : Outliers are not dropped\
    2 : Data is scaled through standard scaler before training the model\
    \
\pard\pardeftab560\slleading20\partightenfactor0

\f0\b \cf0 Fourth Model:\
\pard\pardeftab560\slleading20\partightenfactor0

\f1\b0 \cf0 The model is trained using PCA componets. The merged dataframe is traing using only two PCA componets instead\
of keeping all the features. Still the accuracy score is satisfied.\
\pard\pardeftab560\slleading20\pardirnatural\partightenfactor0
\cf0 \
\pard\pardeftab560\slleading20\partightenfactor0

\f0\b \cf0 Fifth Model:\
\pard\pardeftab560\slleading20\partightenfactor0

\f1\b0 \cf0 The very last model implemented on both types of data and performed PCA and manual feature removal to\
reduce the dimension of the data.\
Steps Performed: 1 : Reduce the dimentionalty of the accelometer data to 3 features instead of 13. 2 : Merged the data from parquet and csv files. 3 : Removed the null values for the target column. 4 : Create the mapping for null values. 5 : Impute the missing values and encoded the fatures thorugh onehotencoder and standard scale implemented thorugh pipeline. 6 : Fit and train the model. 7 : Predict and visualize the accuracy socre.\
\pard\pardeftab560\slleading20\pardirnatural\partightenfactor0
\cf0 \
}