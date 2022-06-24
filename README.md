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
### Deliverable 1: Summary of data

The data provided included the city, date of ride, fare, ride ID, number of drivers that day, and the type of city (urban, suburban, rural). These data were grouped to determine the total number of rides, *total drivers*, and total fares collected for all dates. Note: the total drivers is actually based on an estimation of the average number of drivers per city, since adding all of the data together would be counting the same drivers multiple times each night. This will be further examined in the Code Analysis. From those values, the averages were calculated, and the data were formatted in a summary dataframe as shown below:


![Deliverable1](https://user-images.githubusercontent.com/33167541/175441634-60d49cf1-9ae6-4a32-aefd-f70c8450297d.png)


The cities with the lowest overall fares are the Rural cities, followed by the Suburban and then Urban. But what needs to also be considered are the fares per ride and driver in these regions. While the total fares collected in the Rural cities make up about 11% of those collected in the Urban cities, the Rural fares per ride are 41% higher than those in Urban cities, and even more pronounced are the fares per driver: 235% higher than those collected in Urban cities. What may be of higher concern is that the number of drivers actually providing rides is extremely low. The rural cities averaged 1.6 rides per driver, the suburban cities averaged 1.3 rides per driver, and the urban cities averaged 0.8 rides per driver - meaning some of the drivers available never actually drove anyone! While this doesn't change anything about the fares collected during the rides, it shows the lack of strength that the fares per driver holds, given the assumption that drivers are only compensated when they actually provide a ride.   


### Deliverable 2: Visualize regional total fares over time

Starting with the same merged data that the summary was created from, the data were reconstructed in a pivot table, and the dates were reformatted to datetime format so that the total fares could be grouped per week rather than plotting each specific timepoint. After reforming the data, they were plotted using matplotlib. 

![Deliverable2](https://user-images.githubusercontent.com/33167541/175448730-7cd2cdec-4ddc-46ec-ba56-ebd8e317ae43.png)


Looking at this data over time, it further confirms the findings of the totals throughtout the timeperiod that the urban total fares collected are higher, even on a weekly basis, than the suburban, which is higher than the rural. An interesting observation is that the third week of February was one of the highest fare collections of the entire dataset in all three regions. Within this week, only a few holidays of note occur: Cow Milked While Flying in an Airplane Day falls on the 18th, President's Day is on the 20th, and on the 21st is Fat Tuesday/Mardi Gras. In further analysis, it could be easily determined which of the days is the highest grossing day in February, but it is probably safe to say that most of the rideshares were on ~~Cow Milked While Flying in an Airplane Day~~ Mardi Gras. 


---
## Summary

Based on these data, the total net income from urban cities is far higher than the rural region and even substantially outperforms the suburban regions. This is likely due to the number of users who use PyBer as a means of transportation because they don't need where they live and thus use PyBer for any trips that are beyond walking distance or inconvenient on public transit. Suburban users are much more likely to own a car and only use PyBer for outings where parking is inconvenient or when they know that they will not be able to legally drive. While this is also the case with rural drivers, there are just fewer people living there that the demand is very low in comparison to the suburban and urban demands. Because of the low demand in the suburban and rural regions, the consumers are willing to pay more for their rides, whereas the urban users are less likely to be using the service for social events and more likely to be using the service to avoid needing a vehicle. 

As a suggestion to the CEO of PyBer, increasing the rates of rural fares is not going to bring in much more income, and it is likely to discourage rural riders to use the service. Likely, increasing fares for urban drivers is likely to drive them to the competition, because many urban users are using the service out of necessity, and a replacement of calling a taxi service. If the rural users and suburban users probably have the same reasons for use, since almost all of them need a car to get around those cities, so increasing the rates of the suburban users to that of the rural users would be a good way to raise the overall fares for those cities. Additionally, pushing to advertise using PyBer in urban cities can make a huge difference. Even lowering the fare to be more competitive in the urban regions is still likely to bring in more net income, especially since there are so many drivers available who aren't providing the ride service to consumers. 
