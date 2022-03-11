# Surfs_up

**Overview of the analysis**
The purpose of this analysis is to help W. Avy, a potential investor for our Ice Cream and Surf shop in Hawaii, determine if the investment will be successful based on weather patterns. For our challenge, W. Avy requested that we provide temperature data for the months of June and December in Oahu. In order to do so, we will be using the hawaii.sqlite data file within Jupyter Notebook (6.4.5) in combination with our dependencies numpy, datetime, and pandas. 

**Results**

#Deliverable 1- Finding the average Weather statistics for June#

Instructions: Using Python, Pandas functions and methods, and SQLAlchemy, you’ll filter the date column of the Measurements table in the hawaii.sqlite database to retrieve all the temperatures for the month of June. You’ll then convert those temperatures to a list, create a DataFrame from the list, and generate the summary statistics.

I first imported the sqlalchemy extract function. Next, I created a session query that determines all temperatures within our database from the month of June. The code for these functions can be seen below: 
<img width="902" alt="Screen Shot 2022-03-11 at 11 56 09 AM" src="https://user-images.githubusercontent.com/96043107/157933775-2d61356b-9b8e-4dcf-bb54-12b9170613ab.png">

Next, I converted the temperature data into a list, and then put this list of temperature data into a dataframe. This allows us to retrieve the summary statistics from our temperature list from the month of June, and we do so by using the .describe() function on our Junedf dataframe, as seen in the code below: 
<img width="903" alt="Screen Shot 2022-03-11 at 11 58 20 AM" src="https://user-images.githubusercontent.com/96043107/157934050-2679ae2b-4640-412b-9169-2cd239560463.png">

Finally, deliverable 1 is complete and the summary temperature statistice for the month of June are seen in the table below: 
<img width="115" alt="Screen Shot 2022-03-11 at 11 59 33 AM" src="https://user-images.githubusercontent.com/96043107/157934227-ad0cd554-ee88-4fe9-b7a2-79bb6fa5e802.png">

#Deliverable 2- Finding the average Weather statistics for December#

Instructions: Using Python, Pandas functions and methods, and SQLAlchemy, you’ll filter the date column of the Measurements table in the hawaii.sqlite database to retrieve all the temperatures for the month of December. You’ll then convert those temperatures to a list, create a DataFrame from the list, and generate the summary statistics.

Since we already imported the sqlalchemy extract function in deliverable 1, I can skip this step and create a session query that determines all temperatures within our database from the month of December. The code for these functions can be seen below: 
<img width="905" alt="Screen Shot 2022-03-11 at 12 01 41 PM" src="https://user-images.githubusercontent.com/96043107/157934485-999c8b1a-551e-40c4-b80c-dc42cc7838cf.png">

Next, similar to steps taken in deliverable 1, I converted the temperature data into a list, and organized it into a dataframe, with column names 'Date' and 'Temperature'. Lastly, we can use the .describe() function on our December dataframe to get the summary temperature statistics for the month of Decemebr. These steps of code can be seen below:
<img width="904" alt="Screen Shot 2022-03-11 at 12 04 15 PM" src="https://user-images.githubusercontent.com/96043107/157934815-01558466-7aad-4c6b-8047-639db13421e8.png">

Finally, deliverable 2 is complete and the summary temperature statistics for the month of Decmeber are seen in the table below: 
<img width="116" alt="Screen Shot 2022-03-11 at 12 05 01 PM" src="https://user-images.githubusercontent.com/96043107/157934900-1b05e18f-500d-455b-b053-c9ddc4734cd5.png">

#Differences in weather between June and December#
*The mean Temperature in June (74.94) is about 4 degrees higher than in December (71.04)
*The minimum temperature in December (56) is 8 degrees lower than in June (64), and the maximum temperature in June (85) is 2 degrees higher than in December (83). 
*The number of weather observation points in June (1700) is higher than in December (1517). 

**Summary**
# High level summary of the results:
Since the standard deviation is about 3.25 in June, and 3.75 in December, there is about a 0.5 temperature difference between the two months. Also, we can use June and December as estimates on the general weather patterns for summer and winter. With only a 0.5 difference between the two month's temperature standard deviations, this proves to W. Avy that temperature patterns for this location are relatively mild and mainly consistant throughout the year. 

Two other additional queries that may be helpful would be obtaining weather data for all of the dates of summer (June 21st - September 22) and  winter (December 21 - March 20) and performing similar summary statistics for the full seasons, and not just a month out of each. Note that June and December are both the beginning months for each season, with parts of spring and fall included in the months of June and December as well. 
 
