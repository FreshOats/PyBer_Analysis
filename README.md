# PyBer Rideshare Analysis
*** Evaluating fares for a rideshare company in different city sizes ***
#### by Justin R. Papreck
---

## Overview

Making business decisions on a whim is not just a bad idea, but can end up costing a company millions of dollars or closing the company altogether. Data science is now used by many employers to look at different trends to determine whether these trends are correlational or just happenstance. The rideshare PyBer has set the task to evaluate different city sizes - urban, suburban, or rural - to see trends in the fares and driver numbers. 

### Purpose

Using Python with Pandas, Matplotlib, and Numpy the data were cleaned, evaluated, and then plotted to show the total fare trends by region over time. To do this required merging two dataframes, then grouping the cities by type to determine the total rides, total drivers, total fares, fares per ride, and fares per driver. Next, the data were reorganized in a pivot table, time data reformatted, and finally plotted as a line chart, showing the total fares over time for the 3 city sizes. 

---
## Results and Analysis
### Deliverable 1: Summary of Data

The data provided included the city, date of ride, fare, ride ID, number of drivers that day, and the type of city (urban, suburban, rural). These data were grouped to determine the total number of rides, *total drivers*, and total fares collected for all dates. Note: the total drivers is actually based on an estimation of the average number of drivers per city, since adding all of the data together would be counting the same drivers multiple times each night. This will be further examined in the Code Analysis. From those values, the averages were calculated, and the data were formatted in a summary dataframe as shown below:


![Deliverable1](https://user-images.githubusercontent.com/33167541/175441634-60d49cf1-9ae6-4a32-aefd-f70c8450297d.png)


The cities with the lowest overall fares are the Rural cities, followed by the Suburban and then Urban. But what needs to also be considered are the fares per ride and driver in these regions. While the total fares collected in the Rural cities make up about 11% of those collected in the Urban cities, the Rural fares per ride are 41% higher than those in Urban cities, and even more pronounced are the fares per driver: 235% higher than those collected in Urban cities. What may be of higher concern is that the number of drivers actually providing rides is extremely low. The rural cities averaged 1.6 rides per driver, the suburban cities averaged 1.3 rides per driver, and the urban cities averaged 0.8 rides per driver - meaning some of the drivers available never actually drove anyone! While this doesn't change anything about the fares collected during the rides, it shows the lack of strength that the fares per driver holds, given the assumption that drivers are only compensated when they actually provide a ride.   
