## Project Details

Coflight is about inspecting pricing policies(strategies) of airline companies and proving the rumors are right or wrong on social media which says deleting cookies effects ticket prices. In this project we will check plane ticket prices to see if there's any differences between deleting and not deleting cookies.

The project has 3 main parts

### **1. Scraping** 

Coflight will run on AWS and four airline companies linked below will be scraped by using **Selenium Web Driver**, **Javascript(NodeJS)** and **PhantomJS.**

* ##### [Turkish Airlines](https://www.turkishairlines.com/)
* ##### [Pegasus](https://www.flypgs.com/)
* ##### [Atlasglobal](https://www.atlasglb.com/)
* ##### [Onur Air](https://www.onurair.com/)

Ticket price **currency** should be **TRY**

#### [Here is an example](https://github.com/FCanberk/Scraping/blob/master/Ist_Lon.js)

### **2. DATA COLLECTION**

For each Airline company, 50 flights' ticket price, flight date&time, destination, date&time(UTC +03:00) when these infos taken will be collected every 15 minutes and stored in a database(MongoDB).

### **3. DEMONSTRATING**

Collected data will shown in different graphics for comparing ticket prices with/without deleting cookies and ticket price differences for different time periods.

### Bonus Objectives

* For commonly used destinations ticket prices will graphically shown for whole year.
