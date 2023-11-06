# Project: Crime Data in Los Angeles

This dataset reflects incidents of crime in the City of Los Angeles dating back to 2020 and is provided by Los Angeles Police Department. You can find the database documentation in the website: (https://catalog.data.gov/dataset/crime-data-from-2020-to-present/resource/5eb6507e-fa82-4595-a604-023f8a326099). There are 820K rows and 28 columns in the database. For this reason, we are providing a smaller csv file as a sample so you will be able to run the code. If you would like to see all data, please download the database from the link provided and replace the csv file provided.

For this project we will study 3 main questions:
1) What are the specific profiles that are most vulnerable to be victims of a crime? (sex, age, race)
2) What areas/locations are the most dangerous in LA and the time where most of the crimes occured?
3) Is there a correlation between Weather and time vs Number of Crimes?

Instructions: Find out questions
1) What are the specific profiles that are most vulnerable to be victims of a crime? (sex, age, race).

2) What areas/locations are the most dangerous in LA?
To create this section, we used the time and areas in the database to cross reference with the reported crimes. For simplicity’s sake, the time was divided into 4 sections using bins:
- Dawn (00:00 - 05:59)
- Morning (06:00 - 11:59)
- Evening (12:00 - 17:59)
- Night (18:00 - 23:59)

This allows the data to be more visually friendly and allows the user to get a general understanding of when most of the crimes occur. Findings included that the most crimes that occur in LA happen during the evening and the least amount of them occur at dawn.

To graph the worst area, the database included an area name column and a simple group by allowing the code to filter out all data that did not occur in the evening and graph it. Unsurprisingly, most of the crime that occurs in the evening, occurs in central LA, with 77th street close behind.
After generating both graphs, the program automatically saves these charts to a output folder for easy access to results.

3) Is there a correlation between Weather and time vs Number of Crimes?

To answer this question we are using historical weather data obtained through an API from the website https://open-meteo.com/. The goal was to extract the temperature of the day and time at which the crime occurred, in order to analyze if there is a relationship between temperature and the number of crimes. In order to call the API it was necessary to use a specific format to the dates (YYYY-MM-DD), and also for the time (Provide the time value as an integer).

It is important to mention that due to restrictions on the use of the API and to save computational time, we took a sample of 5000 crimes from the dataset to perform this analysis. As a result of this test, we obtained a correlation of less than 60%, which is not a good value to be able to say that there is a strong relationship between the number of crimes and temperature.

On the other hand, we wanted to analyze the possible relationship between the number of crimes and the time of day. To do this, we simply obtained the number of crimes for each hour of the day and applied linear regression to the data, getting a correlation of 75%, which, although is not a great value, gives us an idea of ​​the behavior of crimes throughout the day.


## Results
it was found that even it is not a crime rule there are certain victim characteristics that are more common among the reports made than others, as in the Victim Profile we can conclude that male people around 30 years old and Hispanic/Latin/Mexican are more likely to be a victim of a crime in Los Angeles City.
![image](https://github.com/Ivanco19/Project-1/assets/74313815/be16b7e2-7291-4211-bd31-ef7cc62e7ae7)
![image](https://github.com/Ivanco19/Project-1/assets/74313815/279fb2e8-62ac-43ee-a607-b40ef0949aa9)
![image](https://github.com/Ivanco19/Project-1/assets/74313815/7b3a8a4c-3401-4344-bd27-2da8427be8bf)





Recommendations for future analysis

For future work with this dataset we recommend carrying out more specific or specific analyses. For example, reducing the analysis to a particular year or month, in locations where crimes occur more frequently or even for a specific sector of the population, for example the age range where people are most vulnerable to being victims of a crime. This could get interesting trends and even more accurate linear regression values.

------------------------------------------------

This code was developed by:
* Iván Corona
* Andrés Elosua
* Frida Ortega
