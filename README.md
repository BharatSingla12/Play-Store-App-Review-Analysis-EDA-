# Exploratory Data Analysis on Play Store App Reviews

## 1. Abstract:
* Google play store is the official app store for all devices operating on the Android OS. It allows the users to browse and download the apps that are developed with the android software development kit (SDK).
* Apart from offering android applications and games, it also serves as a digital media store offering music, books, movies, and television programs.
* User ratings and reviews can significantly increase the number of app downloads; hence it is important to analyse the parameters which lead to users giving positive feedback and higher rating.
* Though this exploratory data analysis, we can understand and discover the key factors responsible for app engagement and success.

## 2. Objective
* To explore and analyze the data to discover key factors responsible for app engagement. 
* To do investigations on data so as to discover patterns, spot anomalies.
* To find conclusions with the help of statistics and graphical representations. 
* To discover key factors that can drive app-making businesses to success.


## 3.	Data Introduction:

### We are provided with two datasets:
* Play_store_data: It contains the basic details of the app like number of user reviews, ratings, etc.
* User_reviews: It contains the user reviews and its sentiment score for the respective app.


### The contents of play_store_data are:
* App: It contains the name of the app with a short description (optional).
* Category: This section gives the category to which an app belongs. In this dataset, the apps are divided among 33 categories.
* Size: The disk space required to install the respective app.
* Rating: The average rating given by the users for the respective app. It can be in between 1 and 5.
* Reviews: The number of users that have dropped a review for the respective app.
* Installs: The approximate number of times the respective app was installed.
* Type: It states whether an app is free to use or paid.
* Price: It gives the price payable to install the app. For free type apps, the price is zero.
* Content rating: It states which age group is suitable to consume the content of the respective app.
* Genres: It gives the genre(s) to which the respective app belongs.
* Last updated: It gives the day in which the latest update for the respective app was released.
* Current Ver: It gives the current version of the respective app.
* Android Ver: It gives the android version of the respective app.

### The contents of user_reviews are:
* App: It contains the name of the app with a short description (optional).
* Translated_Review: It contains the English translation of the review dropped by the user of the app.
* Sentiment: It gives the attitude/emotion of the writer. It can be ‘Positive’, ‘Negative’, or ‘Neutral’.
* Sentiment_Polarity: It gives the polarity of the review. Its range is [-1,1], where 1 means ‘Positive statement’ and -1 means a ‘Negative statement’.
* Sentiment_Subjectivity: This value gives how close a reviewer’s opinion is to the opinion of the general public. Its range is [0,1]. Higher the subjectivity, closer is the reviewer’s opinion to the opinion of the general public, and lower subjectivity indicates the review is more of a factual information.



## 4.	Steps involved:

This Project is segregated into many sections and they are :
* Loading Libraries and Dataset
* Data Exploration
* Data Cleaning
* Data Preparation
* Data Visualization

### 4.1. Loading Libraries and Dataset
I loaded the necessary libraries for the analysis, in which we used Libraries like **Numpy for numerical operations and for n-dimensional arrays**, **Pandas for Data Manipulation and Analysis** and **Matplotlib and Seaborn for Data Visualization**.

I loaded two dataset i.e. Play Store Data and User Review. Play Store Data consisted of columns that were related to the apps like **app size**, **number of installs**, **app category**, **app name**, etc. and User Review consisted of columns like **app name**, **translated review**, ***sentiment*, etc. I loaded the data using the read_csv function of the Pandas library.

### 4.2. Data Exploration
In this step I explored the previously loaded datasets and tried to find some insights from the data. I found that Play Store Data had 1 column with float datatype and 12 columns with object datatype and User Reviews had 2 columns with float datatype and 3 columns with object datatype. Pandas has functions like head(), tail(), info(), describe(), etc. that help us to explore the data and understand the data.

### 4.3. Data Cleaning
In this step I looked for null and missing values by using isnull() and sum() functions on the Play store data and user reviews dataset. I found that Play store data had about 1473 null values in Ratings column, 1 null in Type and Content_Rating columns each and 3 null values in Android_Ver column and User reviews had about 26868 null values in Translated_Review column and 26863 null values in Sentiment, Sentiment_Polarity and Sentiment_Subjectivity columns each. I handled these null by either replacing them or removing the rows that consisted these null values.

### 4.4. Data Preparation
Here I checked if all the columns have appropriate datatypes and handled unnecessary duplicate values in columns as they would cause redundancy in the data.

### 4.5. Data Visualization
Finally I used Matplotlib and Seaborn to plot visuals to understand the data and find insights in the data. The plots that were used are bar plots, pie plots, scatter plots, etc. 
From these we were able to draw conclusions that would help to know the important features for app engagement.




##  5. Final Conclusion
The app engagement and success can be expressed with the app’s total installs and the revenue it generating. 



- The demand of free apps is higher than the paid apps, so you can give priority to free apps.
- In free apps, the category of Communication, Social, Game, Productivity, and Tools will be the best choice to increase the app install.
- In paid apps, the category of Game, Family, Photography, Personalization, and Tools will be the best choice to increase the app install.
- In paid apps, the category of Lifestyle, Finance, Family, Game, Photography will be the best choice to increase the app Revenue.
- In free apps, the genre of Communication, Social, Productivity, Photography and Tools will be the best choice to increase the app install.
- In paid apps, the genre of Action, Action & Adventure, Arcade will be the best choice to increase the app Revenue.
- In Free apps, the content rating of Everyone, and Teen will increase the app installs and in paid apps, the content rating of Everyone 10+, Mature 17+ will increase the app installs.
- An quality app in the lowest rating apps genre or category like Dating, Maps & Navigation, Video players can give a fruitful result.
- Apps like Helix Jump, Duolingo, Calorie Counter, Bowmasters, 10 Best foods for you, google photos, Bfit Workouts & Meal Planner have highest number of positive reviews.
- The median size of paid apps is 9 MB, and the median price of paid app is $2. The median size of free app is 12 MB.
- In top 100 revenue making apps, apps from the category Lifestyle, Finance, and Family have highest average revenue per app.
- In top 100 revenue making apps, apps from the content rating Everyone, Everyone 10+  making highest total revenue but apps for Everyone 10+, Mature 17+ are very limited therefore the average revenue per app in content rating Everyone 10+, Mature 17+ is highest. These two category should be preferred.
In top 100 revenue making apps, apps from the genre Arcade;Action & Adventure, Lifestyle, Finance have highest average revenue per app.
