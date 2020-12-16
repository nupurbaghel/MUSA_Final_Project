# MUSA_Final_Project - 
 ## Forecast Metro train delays in and around NYC
 <hr>
  
  The link to our youtube video: https://youtu.be/1iJWN-v1mvI
  
  ## Introduction
  NJ Transit is considered to have very complex dynamics affecting tens of thousands of people everyday as per a blog post. And it is the case with numerous other transit systems too. Many people rely on these transportation systems for their daily commute and delays may leave them irritated and dissatisfied with the system. Train delays leading to missed connecting trains/flights, miss opportunities, etc. may drive away customers, who are a key source of income here. One way this can be dealt with is by making sure that all trains are on time. But, in this non-ideal world, it is really difficult to maintain such perfection due to various unforeseen circumstances. Thus, train delay predictions come into the picture. We do have many apps that track the status of the trains live, but such applications will not help users plan their trips early on.   

  As already mentioned, trains delays are a cause of concern for many commuters as it is pretty random, or at least that is what it seems like to some people. Train delays can definitely be predicted to some extent provided there is up-to-date accurate data to learn the patterns from. Most times, train delays are due to random problems such as fallen trees blocking the track or technical issues with the train which can be approximated with the utilization of certain variables, which we have capitalized on in this project. These predictions can be used either by the commuters or by the authorities. The application will help the users commute reliably and more effectively, allowing them to plan hours or days prior to their journey, allowing them to make informed decisions. They can schedule their trips efficiently and choose days with low probability of delay if they have a flexible appointments or choose earlier trains to make it to their destination on time. This application can also be used by the authorities to counter expected train delays. But we will be focusing in designing an application to help the commuters.
  
 For more details, look into the rmd / html files. 

## Main Files
- main.Rmd : This RMarkdown contains the project code along with answers to questions asked for in the project requirement.
- main.html : This is the knitted format of the markdown file

## Data 
-  archive : This is the Kaggle dataset provided to us. It contains train delay information for the years 2018-2020. For our project we only use data for April 2018. (For the purpose of lag calculation, we also look at March 2018 data)
- Railroad_Stations_in_NJ-shp : This shapefile contains Geospatial locations for stations belonging to New Jersey Rail Transit Network.
- Amtrak_Stations-shp : This contains Geospatial locations of all Amtrak trains across US (only used for viz in this project) since Amtrak trains were missing delay information.
- Passenger_Railroad_Lines_in_NJ-shap : This contains Geospatial locations of different Rail lines in the NJ Transit network. 

## Feature Engineered Variables (cached)
- lag_variables.csv : Contains the lag pertaining to 1 day, 1 week and 2 weeks for every journey recorded in our dataset in April 2018.
- lag_variables_week.csv : This is a subset of the lag_variables.csv features containing only 1 week and 2 week lags
- dist_variable.csv : This contains distance in meters between every 2 consecutive station journey in our dataset
- diff_delay_variables.csv : This contains the actual delay between every 2 consecutive stations (excluding the cumulative delay from previous station)

## Other files
- trains_local.gif : Contains animation of Congestion variables (number of trains per hour for every station)
- actual_map_station.JPG : A screenshot of the areal view showing the span of Philadelphia, New Jersey and New York states (blue box), versus the span of NJ Transit network (orange box). Stations are also plotted.
