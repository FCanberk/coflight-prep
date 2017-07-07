## **Data Collection Guideline**

### **Querying**

Every five minutes, all flights in [dataset](!!FlightListLinkiEklenecek!!) will be queried.

### **Updating Departure Dates**

Dataset will be dynamic. For that reason dataset have to be updated periodically.

These are the steps should be followed everyday to update departure dates:

1. Get current date once in a day.
2. Calculate date difference between current date and latest flight for every destination.
3. If date difference between latest flight's departure date and current date is lesser than 30 days
4. Then add a flight to that destination 33 days after current date.
5. Calculate date difference between current date and earliest flight for every destination.
6. If date difference between earliest flight's departure date and current date is lesser or equal one day
7. Then stop querying that flight.

#### Exceptional Situations

* While updating departure dates, after the step 3 there might be no flights on the date that we queried. In this case, one day should be added to the queried date until a flight can found.
* There might be no tickets for a flight that we queried. In this case, querying the flight should be stopped and the flight should be deleted from dataset.
* A flight may be cancelled. In this case the flight should be deleted from the dataset and database.

### Examples

Here is an imaginary table for better understanding of how to collect data. It is assumed that today's date is **`2017-07-21`** there should be a table like this

| Destination |Flight 1|Flight 2|...|Flight 10|
|-------------|--------|--------|---|--------|
| IST-MLX     |2017-07-25 /15:30|2017-07-28 /22:50|...|2017-08-21 /16:15|

According to the table above we can see that last flight on `IST-MLX` destination is `Flight 10` and departure date is `2017-08-21` and current date is `2017-07-21`. Date difference between current date and earliest flight is 31 days. One day later, the date difference will be 30 days and one more flight will be added `IST-MLX` destination.

So, on `2017-07-22` table should be like this

| Destination |Flight 1|Flight 2|...|Flight 10|Flight 11|
|-------------|--------|--------|---|---------|---|
| IST-MLX     |2017-07-25 /15:30|2017-07-28 /22:50|...|2017-08-21 /16:15|2017-08-24 /05:35|
If there would be no flights on `2017-08-24` then flights on `2017-08-25` would be queried.

Here is another example.

Let's assume the date is **`2017-07-21`** again. There is an alternative table below

| Destination |Flight 1|Flight 2|...|Flight 10|
|-------------|--------|--------|---|--------|
| IST-MLX     |2017-07-22 /15:30|2017-07-25 /22:50|...|2017-08-23 /16:15|

According to the table above we can see that last flight on `IST-MLX` destination is `Flight 1` on `2017-07-22`. One day later, date difference between earliest flight and current date will be less than one day. Then first flight will be deleted on `IST-MLX` destination and no more queries will be done for this date.

And new table on `2017-07-22` will be like this

| Destination |Flight 1|Flight 2|...|Flight 10|
|-------------|--------|--------|---|--------|
| IST-MLX     |2017-07-25 /15:30|2017-07-28 /22:50|...|2017-08-23 /16:15|
