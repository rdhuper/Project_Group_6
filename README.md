# Project_Group_6 - Project #1

## Which City Would you Choose?
### Alex Barrera, Rohan Dupher, Christina Vavoulis

-----------------------------------------

#### Overview

For this project we used city data from the Teleport API to attempt to answer various questions about global cities, such as: 
Are there patterns between cost of living and taxation, economy and environmental quality, and so on across global cities?
What are the best and worst cities for qualities like Safety, Healthcare, and Housing?
What else can we learn about cities around the globe using this rich data source?



#### Prereqs 

For this project, we used a Jupyter notebook to run our Python code. We used common data modules such as numpy, pandas, and matplotlib. 
We used the free Teleport API for all of our data collection and Google's GEO API for heat map visualizations. 

#### Methodology & Process 

We pulled 100+ metrics for 270 available cities from Teleport's API. 
The first API call collects a list of all cities available and stores in an array.
The second API call requests the Teleport City Scores for each city in the array. These are proprietary scores provided by Teleport that represent several more city attributes (100+) rolled up. These scores are 0 to 10 (0 = less desirable, 10 = most desirable) for location attributes (latitude and longitude) and meta attributes like cost of living, safety, education, healthcare, environment, economy, and more. 
The third API call is a request for a full list of each city's detailed attributes such as days of sunshine, number of libraries, number of schools, LGBT tolerance, average temperature, and many more. This could provide extremely detailed data for each city and would open doors to better visualizations and more accurate statistical testing of our hypothesis. 
Unfortunately, during QA we noticed the JSON results for each city was vastly different and poorly organized, with no clear structure and no conventional labeling. There was an attempt to parse this to be able to use the data, but were advised by the experienced that this could potentially lead to many more hours of work. Thus we abandoned this rich data in favor of the original Teleport Scores.


#### Data Processing

After pulling the city API data from JSON into arrays, we loaded them into dataframes for processing. Initially we explored the datasets by sorting for various attributes and sanity checking the data quality. We also checked the coordinate data before attempting to plot geographic visuals. 

We built scatter plots to test our hypotheses and see if there were visual indicators of trends between expected attributes, such as 'economy' and 'business freedom.' Although for some individual cities the data trended together, we were surprised that most of our charts showed little to no association between all of the predicted relationships. Since this original analysis used the Teleport summary scores, we then decided to pull the 100+ additional variables. 

After pulling the additional city variables, discovering the flaws, and then spending a full day's work and more attempting to salvage that data, we cut our losses and returned to the original data pull. Using the coordinates and the Teleport Scores, we made heat maps using the Google Maps Geo API. These were interesting for a few attributes but ultimately not very striking or informative. We believe this to be another result of using scores from 0-10 instead of actual numeric data. 


#### Retrospective

We had a successful project despite several setbacks:

* Finding datasets. We shifted project ideas several times due to a lack of clean, usable data that wasn't prohibitively expensive. 

* API troubles. We got lots of practice parsing JSON and using a new API. We learned how to use documentation and a lack thereof. Most of all, we learned that not every API has reliable or professionally structured JSON, so it's of utmost importance to quality check as a group instead of assuming any reliability from the developer. 

* Time Management. We got a great head start pulling basic data early in the project, and this ultimately paid off dividends - especially when we could not rely on the richer data source that we made a strong effort to gather and use. This gave our group extra time to align around the project, learn the various aspects, collaborate, and finalize our presentation without having to work late a single night or at the last minute. 


#### Shout Outs

* Group 6 - Rohan, Christina, and myself - great job, guys! 10/10 would work with again.

* Jerome, Jimmy, Eric, Robert - thanks for our endless questions about Git, APIs, JSON, and so much more. 

* Germany and Japan - for being the safest cities with rocking economies in the world.




#### Teleport API

* [Teleport API Documentation](https://medium.com/@ashk3l/a-visual-introduction-to-git-9fdca5d3b43a)

#### Google GeoCoding API

* [Google GeoCoding API Documentation](https://developers.google.com/maps/documentation/geocoding/start)

