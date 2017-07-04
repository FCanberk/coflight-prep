## Project Details 

Coflight is about inspecting pricing policies (strategies) of airline companies and proving the rumors are right or wrong on social media which says deleting cookies effects ticket prices.

In this project we will check plane ticket prices to see if there's any differences between deleting and not deleting cookies. 

<br>With the data we collect we will also be able to answer these questions
<br>When is the cheapest and the most expensive season to buy any plane ticket ?
<br>When is the cheapest and the most expensive price to buy a plane ticket according to time left before take off ?

Flight data of four airline companies linked below will be scraped:

* #### [Turkish Airlines](https://www.turkishairlines.com/)
* #### [Pegasus Airlines](https://www.flypgs.com/)
* #### [Atlasglobal](https://www.atlasglb.com/)
* #### [Onur Air](https://www.onurair.com/)


For each airline company ticket price, flight date&time, current date&time and destination should be scraped.

For Turkish Airlines 20 International 30 Domestic flights,
<br>For Pegasus Airlines 20 International 20 Domestic flights,
<br>For Atlas Global     15 International 15 Domestic flights,
<br>For Onur Air         15 International 15 Domestic flights data 
will be scraped with and without deleting cookies.<br/>

### **Collecting Data**

These data will be scraped every five minutes of everyday. Scraped data from airline companies will be stored in database. The database will store ticket price, flight date&time, destination and date&time (UTC +03:00) when scraped infos taken. MongoDB will used as database in this project.

### **Demonstrating**

Collected data will be demonstrated in different graphics to compare ticket prices with and without deleting cookies and to see ticket price fluctuation for different time periods.

* Daily ticket price,
* Weekly ticket price,
* Monthly ticket price, 
* Yearly ticket price graphics will be demonstrated.

### Bonus Objectives

* Ticket price of same destination for different departure times will graphically shown for whole year for each company. To see which season of year has the cheapest/the most expensive tickets.

* Ticket price of same destination and same flight will graphically shown for whole year for each company. To see when is the cheapest/the most expensive ticket for a particular flight.
