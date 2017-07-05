## Scraping Guide

This guide describes scraping process for Coflight project. It defines input formats to be passed and output formats to be emitted.

### Input Format

Input format will be CSV and it will include
<br>Departure airport code, arrival airport code, departure date and time, return date and time, cookie info
<br>values in written order.

Sample input format for one way trip without cookies
<br>`IST,ADA,20170928-1530,,NC`

Sample input format for round trip with cookies
<br>`IST,BEG,20170928-2250,20170930-0010,YC`

### Output Format

Output format will be CSV and it will include
<br>Departure airport code, arrival airport code, departure date and time, return date and time,current date and time, one way/roundtrip info, cookie info, ticket price
<br>values in written order 

Sample output format of one way trip with cookies
<br>`SAW,OTP,20170327-2300,,20170705-1247,OW,YC,127.99`

Sample output format of round trip without cookies
<br>`LHR,IST,20171230-0515,20180105-1500,20170705-1247,RT,NC,215.00`