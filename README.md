# Module 9 - Surfs's-Up Challenge

## Overview:
The purpose of this challenge is to practice using the SQLAlchemy module in order to parse through data through a SQLite file.

In this particular case, we want to query the hawaii.sqlite database for all the temperatures recorded in June and December in the island of Oahu. From the resulting data retrieved from each SQLite query, we then determine the averages, minimum temperature, maximum temperature, and standard deviation of all temperature data points from the two sets.

---
## Results
The differences between the weather in June and December are as follows:
- There were 1,700 temperatures recorded for the month of June and 1,517 temperatures recorded for the month of December. A 183 data count difference.

- The mean temperature for June was 74.94 degrees F. For December, it was 71.04 degrees F.

- The maximum temperature for June was 85.00 degrees F. For December, it was 83.00 degrees F.

- The minimum temperature for June was 64.00 degrees F. For December, it was 56.00 degrees F.

## June Temperature Averages 
![June Averages](https://github.com/namin1993/surfs_up/blob/9d52cc07338e8f79bac8ac8a7ec2afb6b937d9f5/Resources/June_average_temps.png)

## December Temperature Averages
![December Averages](https://github.com/namin1993/surfs_up/blob/2d9c284c7751ab0d6ca533af46b0ed84b2bd8edb/Resources/December_average_temps_fixed.png)

---
## Summary
According to all temperature results in the summer and winter months from June and December respectively, Oahu appears to be the ideal location to set up a surf shop business.

However, it would important to retrieve more data on the precipitation between June and December by creating these queries:

Query 1  
```
june_results = session.query(Measurement.prcp).filter(func.strftime('%m', Measurement.date) == '6').all()
```

Query 2  
```
december_results = session.query(Measurement.prcp).filter(func.strftime('%m', Measurement.date) == '12').all()
```
