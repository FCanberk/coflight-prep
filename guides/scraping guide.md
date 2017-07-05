## Scraping Guide

This guide describes scraping process for Coflight project. It defines input formats to be passed and output formats to be emitted.

### Input Format

Input format will be in CSV format and it will include the following in the written order

* Departure airport code
* Arrival airport code
* Departure date and time
* Return date and time
* One way/roundtrip info
* Cookie info values

Sample input format for one way trip without cookies

`IST,ADA,20170928-1530,,OW,WC`

Sample input format for round trip with cookies

`IST,BEG,20170928-2250,20170930-0010,WOC`

### Output Format

Output format will be in CSV format and it will include the following in the written order

* Departure airport code
* Arrival airport code
* Departure date and time
* Return date and time
* Current date and time
* Ticket price

Sample output format of one way trip with cookies

`SAW,OTP,20170327-2300,,20170705-1247,127.99`

Sample output format of round trip without cookies

`LHR,IST,20171230-0515,20180105-1500,20170705-1247,215.00`