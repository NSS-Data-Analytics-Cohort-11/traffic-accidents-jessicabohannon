# Nashville Traffic Accidents

For this exercise, you have been provided a dataset of traffic accidents that occurred in Davidson County which was retrieved from https://data.nashville.gov/Police/Traffic-Accidents/6v6w-hpcw. 

This spreadsheet has been divided into the following sheets:
* Accidents: Contains the raw data for each accident. In order to familiarize yourself with what is contained in each column, take some time to review the data dictionary here: https://data.nashville.gov/api/views/6v6w-hpcw/files/3af9281b-fa4f-4044-83f8-1b9a46cc6e95?download=true&filename=Traffic-Accidents-Metadata-v2.pdf.
* Analysis: This sheet will hold most of your answers.
* Zero Car Crashes: This sheet will be used in question 3.
* Collision Types: Contains the text description of each collision type. You will fill in your answers for question 5 here.
* Weather Types, Illumination Types, and Harmful Types: Contain descriptions for the other three codes. Not used in this exercise.

Use formulas to answer each question. Unless otherwise stated, fill in your answers in the "Analysis" tab.

1. How many total accidents are contained in this dataset?

2. What are the earliest and latest records that appear in this dataset?

3. a. Create a new column to the right of the "Number of Motor Vehicles" column called "Single or Multiple". This column should contain "Single" if the number of vehicles is 1 and "Multiple" if it involved more than one vehicle.  
b. Are there any rows that involved zero vehicles? How many? Make sure that your formula accounts for these cases.  
c. Investigate the rows that have zero vehicles using the FILTER function in the "Zero Car Crashes" sheet. What do you find?  
d. What percentage of crashes are single-car?

4. How many accidents occurred which are hit and run and had at least one injury?

5. a. What is the overall average number of injuries?  
b. Go to the "Collision Types" sheet and fill in the table to find the total number of crashes, average number of injuries, and total number of injuries per collision type. For each calculation, write a single formula and copy it down the table. What do you find? (Hint: If you're not sure how to answer this question, revisit the "Conditional functions and lookups" chapter of [Data Analysis in Spreadsheets](https://app.datacamp.com/learn/courses/data-analysis-in-spreadsheets).)

6. Add four new columns, Month, Year, Hour, and Weekday to the right of the Date and Time column. Use the [TEXT function](https://support.microsoft.com/en-us/office/text-function-20d5ac4d-7b94-49fd-bb38-93d29371225c) to extract out the Month, Year, Hour, and Weekday from the "Date and Time" column.  

7. Fill in the Hour table in the Analysis spreadsheet to find the number of accidents that occurred for each hour of the day. Again, write a single formula and copy it down the table. Do you see anything unusual? What might be the explanation for this?

8. Do the same for the year and day of the week. What stands out?

9. Add a column to the right of the Collision Type Code called "Collision Type". Use the table contained in the Collision Types sheet to fill in this column. 

10. Which interstate has the most accidents between I-24, I-40, I-65, and I-440? Answer this by counting the number of accidents that contain the strings "I 24", "I 40", "I 65", or "I 440" in their Street Address. Hint: You may need to make use of [wildcards](https://support.microsoft.com/en-us/office/using-wildcard-characters-in-searches-ef94362e-9999-4350-ad74-4d2371110adb) in combination with the CONCAT function to answer this. Then do the same but search for "I24", "I40", "I65", and "I440" and then "I-24", "I-40", "I-65", and "I-440". Sum the results to get a total count. 

Text answers:

* "Investigate the rows that have zero vehicles using the FILTER function in the "Zero Car Crashes" sheet. What do you find?"

See Zero Analysis sheet for visualizations. The majority of Zero Car Crashes were of the Harmful Type "motor vehicle in transport" (count 6369). The next most common Harmful Types were "parked motor vehicle" (count 435), "concrete traffic barrier" (count 282), "utility pole" (count 218), and "guardrail face" (count 199). 

For Collision Types of Zero Car Crashes, "front to rear" was the most common (count 2558), with "angle" (count 2382) and "not collision w/ motor vehicle-transport" (count 1824) coming in next.

* "Fill in the Hour table in the Analysis spreadsheet to find the number of accidents that occurred for each hour of the day. Do you see anything unusual? What might be the explanation for this?"

See Time Analysis sheet for visualizations. When visualizing the Count of Accidents by Hour of Day, you can see that accidents happen least often in the early hours of the morning. There is an increase approaching morning rush hour, with a peak at 7am. Accidents die down a bit during the workday, with a steady rise peaking at 5pm for afternoon rush hour, after which accidents die down again. The sharp jump at hour 0 (midnight to 12:59pm) stands out. A possible explanation would be that drivers going home under the influence of alcohol or sleep deprivation are more likely to have an accident, and are responsible for this jump. Another possible explanation is that when actual accident times are not input correctly, they are entered in as being in the 0 hour as default.

* "Do the same for the year and day of the week. What stands out?"

See Time Analysis sheet for visualizations. 

Year: I notice a slow and steady rise in accidents from 2015 to 2019, followed by a sharp decline in accidents by year in 2020, with declines each year thereafter. A likely explanation would be the increase in remote working during the Covid-19 pandemic beginning in 2020 has resulted in less commuters, and therefore less accidents. Note that this dataset goes through June 2022, so the data for 2022 is not complete, so the actual 2022 accident count is not as low as represented.

Weekday: I notice that Monday through Thursday are relatively similar, with a rise on Friday and a drop on Saturdays and Sundays. A possible explanation for the lower number of accidents on weekends is that there are less commuters on the road. A possible explanation for the higher number of accidents on Fridays is that people are rushing to get home after work. I'd be interested to see the hourly breakdown limited to Fridays and see what times account for the majority of the accidents.


