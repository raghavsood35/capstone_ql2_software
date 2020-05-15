---This is car rental data for 2019, grouped by location, agency, Week of the year and Day of the week. 
---It gives us Count, average, min, maximum, median and standard deviation of daily fare
select location as Location,agency as Agency,extract(week from pdate) as 'Week Number', dayofweek(pdate) 'Day of Week',avg(daily_fare) as Avg_Fare,min(daily_fare) as Min_Fare,max(daily_fare) as Max_Fare,median(daily_fare) as Median_Fare,stddev(daily_fare) as SD_Fare, count(*) as No_Records
from cmu_carrental
where extract(year from pdate) = 2019
group by 1,2,3,4
order by 1,2,3,4;