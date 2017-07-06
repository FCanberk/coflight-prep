## **Data Collection Guideline**

Every five minutes of everyday information of all flights listed [here](!!FlightListLinkiEklenecek!!) will be collected and stored.

Everyday at 00:00 date of the day will be get and checked date difference between current date and the latest departure dates of all destinations on flight list will be queried. If date difference between current date and date of any destination's latest flight is greater than 30 days then a flight should be added in that destination. Added flight's date should be 3 days later than the latest flight. If there is no flight on that date, one more day should be added the latest departure date untill a flight can be found. Additionaly the date difference between current date and earliest departure dates of all destination on flight list will be queried. If date difference is equal or less than one day it means all scraping process of the flight has done and it will be deleted on the table which shows flights that will be queried.


Here is an imaginary sample table for better understanding of how to collect data.
So if it is assumed that today's date is **`2017-07-21`** table of flights that will be queried should be like this

| Destination |Flight 1|Flight 2|Flight 3|Flight 4|Flight 5|Flight 6|Flight 7|Flight 8|Flight 9|Flight 10|
|-------------|------------|------------|-----------|---------------|------------|------------|-----------|------------|------------|------------|
| IST-MLX     |2017-07-25 /15:30|2017-07-28 /22:50|2017-07-31 /16:15|2017-08-03 /21:10|2017-08-06 /03:50|2017-08-09 /12:10|2017-08-12 /08:45|2017-08-17 /15:15|2017-08-20 /18:35|2017-08-25 /11:25
| IST-GTW     |2017-07-28 /19:25|2017-07-31 /22:55|2017-08-02 /06:45|2017-08-05 /15:15|2017-08-08 /10:35|2017-08-11 /12:20|2017-08-14 /08:45|2017-08-17 /16:00|2017-08-20 /23:15|2017-08-23 /19:00|
| BEO-SAW     |2017-07-22 /00:15|2017-07-25 /05:15|2017-07-28 /08:30|2017-07-31 /02:00|2017-08-03 /15:05|2017-08-06 /22:20|2017-08-09 /17:40|2017-08-12 /23:00|2017-08-15 /11:15|2017-08-18 /20:00


According to the table above we can see that Date of `Flight 10` for `IST-MLX` destination should be 2017-08-23 but it is 2017-08-25. The reason of it is there's no `IST-MLX` flight on 2017-08-23 so IST-MLX flights on 2017-08-24 queried and found out there's no `IST-MLX` flight on 2017-08-24 aswell then added one more day to the departure date and a flight found on 2017-08-25 so now the latest flight will be queried for `IST-MLX` destination is 2017-08-25.

Let's take a look at `BEO-SAW` destination. The earliest flight will be queried is `Flight 1` on 2017-07-22, the latest is `Flight 10` on 2017-08-18 and tomorrow's date will be 2017-07-22 in this case. Tomorrow `Flight 1`'s date will be deleted and one more flight on 2017-08-21 will be added on the table. Because date difference between today and the latest flight will become greater than 30.

So tomorrow's table should be like this

| Destination |Flight 1|Flight 2|Flight 3|Flight 4|Flight 5|Flight 6|Flight 7|Flight 8|Flight 9|Flight 10|
|-------------|------------|------------|-----------|---------------|------------|------------|-----------|------------|------------|------------|
| IST-MLX     |2017-07-25 /15:30|2017-07-28 /22:50|2017-07-31 /16:15|2017-08-03 /21:10|2017-08-06 /03:50|2017-08-09 /12:10|2017-08-12 /08:45|2017-08-17 /15:15|2017-08-20 /18:35|2017-08-25 /11:25
| IST-GTW     |2017-07-28 /19:25|2017-07-31 /22:55|2017-08-02 /06:45|2017-08-05 /15:15|2017-08-08 /10:35|2017-08-11 /12:20|2017-08-14 /08:45|2017-08-17 /16:00|2017-08-20 /23:15|2017-08-23 /19:00|
| BEO-SAW     |2017-07-25 /05:15|2017-07-28 /08:30|2017-07-31 /02:00|2017-08-03 /15:05|2017-08-06 /22:20|2017-08-09 /17:40|2017-08-12 /23:00|2017-08-15 /11:15|2017-08-18 /20:00 |2017-08-21 /05:15

### Exit Cases

* No ticket left
* Plane take off date passed
* Flight cancelled
* Scraping process interrupted
