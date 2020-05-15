---This is airfare data for 2019, grouped by Arrival Airport, Carrier, Departure Airport, Week of the year and Day of the week. 
---It gives us Count, average, min, maximum, median and standard deviation of fare
select to_airport as 'Arrival Airport',cxr as Carrier,from_airport as 'Departure Airport',extract(week from ddate) as 'Week Number',dayofweek(ddate) as 'Day of Week',avg(fare) as Average_Fare,min(fare) as Min_Fare,max(fare) as Max_Fare,median(fare) as Median_Fare,stddev(fare) as SD_Fare, count(*) as No_Records
from cmu_airfare
where extract(year from ddate) = 2019
group by 1,2,3,4,5
order by 1,2,3,4,5;
