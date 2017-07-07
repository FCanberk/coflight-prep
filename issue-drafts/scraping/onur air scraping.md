# TODO: canberk - describe the issue

Please refer to [Scraping Guide](https://github.com/FCanberk/coflight-prep/blob/master/guides/scraping%20guide.md) first to see the technologies used and the input / output formats.

Every 5 minutes [Onur Air](https://www.onurair.com/tr/) website will be visited and every flight listed [here](FlightListLink) will be scraped. The output will be sent to orchestrator.

A valid citizenship id number and a valid credit card number will be needed for scrapping. Citizenship id numbers could be generated [here](https://www.simlict.com/tcno.html) and credit card numbers could be generated [here](https://names.igopaygo.com/credit-card).

These are the steps should be followed:

Areas in the circle must be clicked or filled. Areas in rectangle 

Select departure airport, arrival airport, departure date, one way/round trip and if it is round trip select return date. 
![onur-pic1](https://s16.postimg.org/yymvbr6zp/image.png)

Select the flight in available flights.Get the flight date&time inside the ractangle.
![onur-pic2](https://s12.postimg.org/lf9aenw3x/image.png)


if its a one way trip skip this step
![onur-pic2.5](https://s12.postimg.org/lf9aenw3x/image.png)

![onur-pic3](https://s12.postimg.org/wsvtpv6ml/image.png)

![onur-pic4](https://s12.postimg.org/56t256n9p/image.png) 

![onur-pic5](https://s12.postimg.org/my4ojn2od/image.png)

![onur-pic6](https://s12.postimg.org/k5bgzm2bx/image.png)
