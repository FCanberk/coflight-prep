## Project Details for Developers

Coflight will run on **AWS. Selenium Web Driver, Javascript(NodeJS)** and **PhantomJS.** will be used for scraping. **MongoDB** will be used for storing the data that collected. The project has 3 main parts. 

### **1. Scraping** 

**Selenium Web Driver**, **Javascript(NodeJS)** and **PhantomJS.** will be used for scraping flight data of airline companies linked below

* #### [Turkish Airlines](https://www.turkishairlines.com/)
* #### [Pegasus Airlines](https://www.flypgs.com/)
* #### [Atlas Global](https://www.atlasglb.com/)
* #### [Onur Air](https://www.onurair.com/)

Here are scraping guides for [**Turkish Airlines**](https://github.com/FCanberk/coflight-prep/blob/master/issue-drafts/scraping/thy%20scraping.md) ,
 [**Pegasus Airlines**](https://github.com/FCanberk/coflight-prep/blob/master/issue-drafts/scraping/flypgs%20scraping.md) , [**Atlas Global**](https://github.com/FCanberk/coflight-prep/blob/master/issue-drafts/scraping/atlasglobal%20scraping.md) and [**Onur Air**](https://github.com/FCanberk/coflight-prep/blob/master/issue-drafts/scraping/onur%20air%20scraping.md)

Ticket price `currency` will be `TRY`

For each airline company ticket price, flight date&time,current date&time and destination should be scraped.

<br>For Turkish Airlines 20 International 30 Domestic flights,
<br>For Pegasus Airlines 20 International 20 Domestic flights,
<br>For Atlas Global     15 International 15 Domestic flights,
<br>For Onur Air         15 International 15 Domestic flights data 
should be scraped with and without deleting cookies.

These data should be scraped every five minutes of everyday. 

### **2. Collecting and Storing Data**

Collected data will be stored in a document db (most likely MongoDB). Scraped data should be stored in separate databases for each company. Each database should store ticket price, flight date&time, destination, date&time (UTC +03:00) when scraped infos taken.

### **3. Demonstrating**

Collected data should be demonstrated in different graphics to compare ticket prices **with** and **without** deleting **cookies** and to see ticket price fluctuation for different time periods.

* Daily ticket price of same ticket with and without cookies,
* Weekly ticket price of same ticket with and without cookies,
* Monthly ticket price of same ticket with and without cookies, 
* Yearly ticket price of same ticket with and without cookies  graphics should be demonstrated.

### Bonus Objectives

* Ticket price of same destination for different departure dates&times will graphically shown for whole year for each company. To see which season of year has the cheapest/the most expensive tickets.

* Ticket price of one flight will graphically shown for whole year for each company. To see when is the cheapest/the most expensive ticket for a particular flight.
