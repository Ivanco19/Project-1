# Project-1
Instructions: Find out questions
1) What are the specific profiles that are most vulnerable to be victims of a crime? (sex, age, race)
2) What areas/locations are the most dangerous in LA?
To create this section, we used the time and areas in the database to cross reference with the reported crimes. For simplicity’s sake, the time was divided into 4 sections using bins:
- Dawn (00:00 - 05:59)
- Morning (06:00 - 11:59)
- Evening (12:00 - 17:59)
- Morning (18:00 - 11:59)

This allows the data to be more visually friendly and allows the user to get a general understanding of when most of the crimes occur. Findings included that the most crimes that occur in LA happen during the evening and the least amount of them occur at dawn.

To graph the worst area, the database included an area name column and a simple group by allowing the code to filter out all data that did not occur in the evening and graph it. Unsurprisingly, most of the crime that occurs in the evening, occurs in central LA, with 77th street close behind.
After generating both graphs, the program automatically saves these charts to a output folder for easy access to results.

3) What profile is most likely to commit a crime?
4) When the weather is not favorable crime drops
5) What is the most popular crime in LA?
6) Linnear regression: Crimes forecast (Location, time)
