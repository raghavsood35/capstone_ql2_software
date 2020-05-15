--This query retrieves Collect Date, Pickup Date, Drop Date, Outsipp, LOR , Average Daily rental fare along with minimum, maximum and median daily rental fare and counts of the records 
--from CMU_CARRENTAL table. The result has been filtered for Pickup Date in 2018 and 2019 and has been grouped-by COLLECT_DATE,pdate,ddate,outsipp and LOR

select to_date(qts) as COLLECT_DATE,pdate as Pickup_Date,ddate as Drop_date,out_sipp,LOR,avg(daily_fare),min(daily_fare),max(daily_fare),median(daily_fare),count(*) as No_Records
from  "QL2_PROD"."PUBLIC"."CMU_CARRENTAL"
where (extract(year from pdate) = 2019 or extract(year from pdate) = 2018) and location ='LAX' and LOR > 0
group by 1,2,3,4,5
order by 1,2,3,4,5;
