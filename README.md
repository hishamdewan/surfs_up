# Surf's Up with Advanced Data Storage and Retrieval

## Overview of the analysis
The purpose of the analysis is assess if weather condition in Oahu, Hawaii is conductive of operating a surf and ice cream shop would be viable year round. I analyze weather data stored in SQLite file and look at summary statistics of temperature and precipitation during June and December to see if operating a surf shop would be viable year round. 

## Results

- Average temperature in June is approximately 75° F and average temperature in December is approximately 71° F.  
- Temperature in June has lower variability (i.e. standard deviation) than December. 
- June temperature ranges between 64° to 85° F versus December temperature ranges between 56° to 83° F. That is, temperature is ideal for running a surf shop in both June and December. 

Summary statistics of June temperature is shown below:

![Jun_descriptive_stats](/Resources/Jun_descriptive_stats.png)

Summary statistics of December temperature is shown below:

![Dec_descriptive_stats](/Resources/Dec_descriptive_stats.png)

## Summary 
Given range of temperature and average temperature in June and December, the moderately warm weather appears ideal for running a surf shop year round. In addition, I ran the following two queries to get summary statistics on precipitation in June and December. The low average precipitation in June and December appears ideal for running a surf shop year round as well.

1) june_prcp = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 6)

![june_prcp](/Resources/june_prcp.PNG)

2) dec_prcp = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 12)

![dec_prcp](/Resources/dec_prcp.PNG)
