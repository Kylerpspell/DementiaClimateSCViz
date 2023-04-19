# CSCE 567: Final Project Writeup
#### An investigation of Dementia and Climate Relationships
#### Kyler Spell

## Project Proposal:
### Intro/Background
Dementia is an impairment in the ability to think, remember or make decisions. The South tends to
have a high rate of dementia mortality. The purpose of this project is to visualize the data of dementia rates in South Carolina to help determine some factors that may be contributing to the high rate of dementia in the South. One of the factors that may be contributing to the high rate of dementia in the South is the climate. The climate in the South is very hot and humid.This may contribute especially to a specific type of dementia called vascular dementia. Vascular dementia is a type of dementia that is caused by a series of small strokes. The strokes may be caused by the high heat and humidity in the South.

I plan to take data on dementia in South Carolina provided by Maggie Miller from the University of
South Carolina Arnold School of Public Health Office for the Study of Aging. To get climate data I will use the Farmers Almanac website. This way I can poll the historical data for the 20 years prior to the dementia diagnosis date for the zipcode of the patient. I will then compare the dementia rates to the climate data to see if there is a correlation between the two.
### Audience
The Audience for this project is both the general public and the medical community. The general public should be able to learn about dementia and gain awareness of the particularly high rate of dementia in the South. The medical community should be able to learn about the possible correlation between dementia and climate. This could help them to better understand the causes of dementia and possibly help them find innovative ways to prevent dementia in the future.
### Dataset(s):
1.) Dementia data from Maggie Miller (300,000 records including zip code, diagnosis date, and
dementia type as well as other demographic data)
- I will need to clean the data to remove any records that are not in South Carolina as well as
any records that are missing data.
- The zipcodes will need to be trimmed down to the first 5 digits to match the zipcodes in the
climate data.


2.) Climate data from Farmers Almanac website (20 years of historical data for each zip code including
temperature, humidity, and cloud cover; https://www.farmersalmanac.com/weather-history)
- This data can have missing values, for these values I will use the average of the previous and
next values in the time series data.
- This data will need to be collected by a web scraper and then stored in a database.


### Proposed visualizations
1.) A map visualization of the dementia rates in South Carolina. This will be a choropleth map with the dementia rates as the color scale

2.) A map visualization of the temperature data in South Carolina. This will be a choropleth map with the temperature data as the color scale.

3.) A map visualization of the humidity data in South Carolina. This will be a choropleth map with the humidity data as the color scale.

4.) A line graph visualization of the dementia rates over time. This will be a line graph with the dementia rates as the y-axis and the time as the x-axis.

5.) A line graph visualization of the temperature data over time. This will be a line graph with the
temperature data as the y-axis and the time as the x-axis.

6.) A line graph visualization of the humidity data over time. This will be a line graph with the humidity data as the y-axis and the time as the x-axis.

7.) I think a polar area chart would also help display the averages for this cyclical data and would give an overview of the climate during the months of the year. I will use the temperature as my radius axis and the month of the year as the rotational axis. Maybe using small multiples to compare the climate of two zip codes or more.

8.) A scatter plot visualization of the dementia rates vs the statistical summary temperature data. This will be a scatter plot with the dementia rates as the y-axis and the temperature data as the x-axis.

9.) A scatter plot visualization of the dementia rates vs the statistical summary humidity data. This will be a scatter plot with the dementia rates as the y-axis and the humidity data as the x-axis.

### Plan
#### Ambitious plan:
I plan to use Javascript to create the visualizations. The visualizations will be laid out on a
webpage in a way that will provide context for the data. I will use the D3 library to create the visualizations. I
will use the Leaflet library to create the map visualizations. I will use the Dimple library to create the line graph
and scatter plot visualizations. The webpage will have multiple tabs. The first tab will be a general overview of
dementia in South Carolina. The second tab will be a general overview of the climate in South Carolina. The
third tab will be a comparison of the dementia rates to the climate data. There will be a fourth tab that will be a
dashboard. This dashboard will allow the user to select a specific dementia types and compare the dementia
rates to the climate data. The user will also be able to select a specific zip code and compare the dementia
rates to the climate data. Finally there will be a fifth tab that will have sources and contact information for the
data.
#### Fall-back plan
I plan to use Tableau Stories to create the visualizations. The first tab will be a general overview
of dementia in South Carolina. The second tab will be a general overview of the climate in South Carolina. The
third tab will be a comparison of the dementia rates to the climate data. There will be a fourth tab that will be a
dashboard. This dashboard will allow the user to select a specific dementia type and compare the dementia
rates to the climate data. The user will also be able to select a specific zip code and compare the dementia
rates to the climate data. Finally there will be a fifth tab that will have sources and contact information.

### Instructor Feedback
``` text
Nice job!

I suggest including benchmark numbers for dementia rates across the country to add context – to show the relationship between rates in SC vs. the country as a whole. Increases in the rates over time could partially be attributed to increased diagnosis / awareness of the issue, so comparison to an overall rate would be helpful.

I look forward to seeing your work on this project!
```

### Changes to Proposal

I combined the line charts into a single graph and ommited the humidity data. I did this because I was unsure how to add a third axis to the chart. 

I also ommited the polar area chart. This was a techinal and time limitation for me. I completed mock ups for the polar area chart but I wanted to add them to each county on the map, which would have been lots of data processing and a technical challenge. 

I combined the scatter plots into a single graph. 

## Summary/ Visualisation Access:
This project is an investigation of the relationship between dementia and climate. The data used in 
this project was collected from a variety of sources, including the "South Carolina Alzheimer’s Disease Registry" from the South Carolina Arnold School of Public Health, 
the Farmer’s Almanac, and US Census data. 

We start with a brief overview of dementia and its impact on those afflicted. At the bottom of the home page of my visualization is a link to the start of a guided tour through each of my six visualizations.
When a user clicks on that link, they are taken to the first of six visualizations. Each visualization has legends and tooltips to help the user understand the data. The user can also click on the 
"Next" button at the bottom of the page to move to the next visualization.

At the end of the guided tour, the user can navigate to data sources and links to each of the visualizations. The user can also click on the "Home" button at the top of the page to return to the home page.

Overall the visualizations did not find a meaningful relationship between dementia and climate. The data displayed is still interesting and may be useful to researchers in the future.
The site is hosted at [https://kylerpspell.github.io/DementiaClimateSCViz/](https://kylerpspell.github.io/DementiaClimateSCViz/).
## Challenges Encountered:
One of the challenges encountered was the overwhelming amount of data that needed to be collected and organized in a useful way.
First I need to clean the data.
 - The data I got from the Alzheimer’s registry was in a CSV file, but it was not in a format that was easy to work with. I had to clean the data and remove unnecessary columns and records.
 - The data from the farmers almanac was much more difficult to handle.
    - First I needed to determine what years and zipcodes to pull data from. In the end I decided to generate an entire 40 year history of the climate for each zipcode in South Carolina. ~250,000 records.
    - Next the data needed to be scraped from the website as there was not an API to make these requests. I used the python library BeautifulSoup to scrape the data.
    - Each request to the website took about 3 seconds to complete. This would take ~ 8.6 days to complete in serial. I used the python library concurrent.futures to make the requests in parallel. This reduced the time to ~ 3 hours.
    - That data then got stored in a makeshift local database of JSON files. 
    - I then took each alzheimers database record YODX and zipcode to generate the 20 year history of the climate for that zipcode.
    - I then took the 20 year history of the climate for each zipcode and generated the average temperature and humidity.
    - There were then around 98,000 records.
    - For the scatter plot I rendered a svg:circle for each record. This was very slow. I decided to remove very similar records. I created simple reduction script that would determine if a record was within 0.1 degrees of another record. This reduced the number of records to ~ 5,000,
    much more manageable to render.

- Creating each visualization was fairly straight forward barring a learning curve for d3js. 
## Design Decisions:
My first visualization was a simple bar chart designed to compare the average age of diagnosis between this dataset and the national average. This was a simple bar chart with a tooltip to display the exact value. This visualization was a starting point for me as I needed to learn how to use d3js with csvs and how to better utilize animations. 

My next visualization was line graph comparing the number of dementia cases in South Carolina to the average tempurature. I used two lines and two axis with corresponding colors. The axis colors match the line colors. I used a tooltip to display the exact value. This was a difficult visualization because I hadn't made a chart with two axis before.

My third visualization was a scatter plot comparing the tempurature, humidity and type of dementia. This is the visualization with the most complex data as there are three channels of data to parse.
I used basic colors (red, yellow, green, blue) to represent the type of dementia and then the location on each axis to represent the tempurature and humidity. I used a tooltip to display the exact values.

The next three visualizations were the cloropleth maps with different color scales and data. The first being a map of the number of cases. This graph can be normalized to the county population to show the number of cases per 100000 people. The second map was the average tempurature, followed by the average humidity. Each map has tooltips to display the exact value and county name.
## Discussion of Future Work:

I would like to add a small multiples or scatter matrix to the scatter plot visualization. This would allow the user to see the relationship between the three channels of data. I would also like to add a slider to the scatter plot to allow the user to see the relationship between the three channels of data over time.

I think a good next step would to add more climate factors to the dataset, as there may be more interesting relationships between dementia and climate. 

I would also like to add a map of the United States to show the relationship between dementia and climate across the country. This would require a lot more data, but would be very interesting to see.

I would also like to have popups of a climate history for each county when the user hovers over a county on the map.




