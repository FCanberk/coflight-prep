## Project Details

Coflight is about inspecting pricing policies(strategies) of airline companies and proving the rumors are right or wrong on social media which says deleting cookies effects ticket prices. In this project we will check plane ticket prices to see if there's any differences between deleting and not deleting cookies.

The project has 3 main parts

### **1. Scraping** 

Coflight will run on AWS and four airline companies linked below will be scraped by using **Selenium Web Driver**, **Javascript(NodeJS)** and **PhantomJS.**

* #### [Turkish Airlines](https://www.turkishairlines.com/)
* #### [Pegasus Airlines](https://www.flypgs.com/)
* #### [Atlasglobal](https://www.atlasglb.com/)
* #### [Onur Air](https://www.onurair.com/)
#### [Here is an example](https://github.com/FCanberk/Scraping/blob/master/Ist_Lon.js)

Ticket price **currency** should be **TRY**

For each airline company ticket price, flight date&time,current date&time and destination should be scraped.

For Turkish Airlines 20 International 30 Domestic flights,

For Pegasus Airlines 20 International 20 Domestic flights,

For Atlas Global     15 International 15 Domestic flights,

For Onur Air         15 International 15 Domestic flights data 
should be scraped with and without deleting cookies.

These datas should scraped every hour of everyday. By doing this we will have informations like the cheapest ticket can be found on what time of the year or month or week. 


### **2. DATA COLLECTION**

Scraped datas should stored in separate databases for each company. Each database should store ticket price, flight date&time, destination, date&time(UTC +03:00) when scraped infos taken. MongoDB will used as database in this project.

### **3. DEMONSTRATING**

Collected data will be demonstrated in different graphics to compare ticket prices with/without deleting cookies and to see ticket price fluctuation for different time periods.There should be six graphics for same flight-different time periods;
* Ticket price - Days of the week (with cookies)
* Ticket price - Days of the week (without cookies)
* Ticket price - Days of the month (with cookies) 
* Ticket price - Days of the month (without cookies)
* Avarage ticket price - Months of the year (with cookies)
* Avarage ticket price - Months of the year (without cookies)
 
And there should be three graphics for same destination different Departure Date;
* Cheapest ticket price - Days of the week
* Cheapest ticket price - Days of the month
* Avarage  ticket price - Months of the year

### Bonus Objectives

* Ticket price of same destination but different flights in different times will graphically shown for whole year for each company. To see which season of year the cheapest/the most expensive tickets can be found.
* Ticket price of same destination and same flight will graphically shown for whole year for each company. To see when is the cheapest/the most expensive ticket for a particular flight.
