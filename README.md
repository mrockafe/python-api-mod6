# python-api-mod6
Module 6 challenge using api's within jupyter lab

PLEASE READ THE README IN CODE VIEW

In this repositopry we go over weather data pulled from a public api provided by https://openweathermap.org/api and data from the https://www.geoapify.com/ api's
This read me will be a guide to how the repository is set up and how my code works
The repositoty holds all of the data and outputs in the "Starter_code" folder
Within this folder is our two jupyter notebook files, WeatherPY.ipynb & VacationPY.ipnyb, and our output_data folder for exported data from the main code

To begin running this code please clone the entire repository to your local device, the api keys, url, and relative path are set up to run the code once cloned

Begining with the file named WeatherPy.ipynb
  To begin all required libraries are imported and the units are set to metric per the api aand module instructions
  This code uses an api from openweathermap api to gather all of its data into one varriable called "city_data"
  We then take this dataset and create a pandas dataframe with the pulled in data
  Once we have this dataframe we output it back to the repository in output_data as cities.csv
  From here we can create 4 scatterplots comparing latitude to: Tempature(°C), Humidity(%), Cloudiness (%), Wind speed(m/s)
  All 4 of these plots are also exported to the output_data folder as fig1, fig2, fig3, and fig4
  Lastly the data is divided up into two new dataframes to perform linear regression models by the southern hemisphere(Lat < 0) and northern hemisphere (Lat >= 0)
  Once finished we can finish the reression models for latitude to: Tempature(°C), Humidity(%), Cloudiness (%), Wind speed(m/s) for each hemisphere and draw our results

Next we move to the file named VacationPy.ipynb
  To begin this code we will import all required libraries and pull in out cities.csv as a pandas dataframe
  Next we create a Map Plot Scatter Plot for humidity with the points mapped out globally
  Each point is sized based off of the humidity %, the higher the percentage the larger the dot
  From here we can create a new dataframe for cities meeting the ideal weather conditions of: Max temp between 21 - 27 °C, Wind speed less then 4.5 m/s, and 0 cloudieness percentage
  Next we store this data in a new dataframe with a blank column created for Hotel Name
  Lastly we use this data and geoapify to locate the nearest hotel within 10,000 meters of the coordinates and idex the hotel name in the dataframe
  With the dataframe completed we can finish with anew Map Plot plotting the hotel coordinates on our scatterplot map
