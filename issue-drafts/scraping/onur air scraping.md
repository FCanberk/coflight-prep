# TODO: canberk - describe the issue

Please refer to [Scraping Guide](https://github.com/FCanberk/coflight-prep/blob/master/guides/scraping%20guide.md) first to see the technologies used and the input / output formats.

Every 5 minutes [Onur Air](https://www.onurair.com/tr/) website will be visited and every flight listed [here](FlightListLink) will be scraped. The output will be sent to orchestrator.

A valid citizenship id number and a valid credit card number will be needed for scrapping. Citizenship id numbers could be generated [here](https://www.simlict.com/tcno.html) and credit card numbers could be generated [here](https://names.igopaygo.com/credit-card).

These are the steps that should be followed:

**Areas in the circle must be clicked or filled. Areas in rectangle have information to gather.**

Select departure airport, arrival airport, departure date, one way/round trip and if it is round trip select return date.
![onur-pic1](https://s10.postimg.org/hdzbrmy7t/image.png)

Select the flight in available flights. Get departure date&time.
![onur-pic2](https://s4.postimg.org/60e1a55e5/image.png)

If it will be one way trip skip this step, otherwise, select return flight.
![onur-pic2.5](https://s4.postimg.org/idqvh1v2l/o2.5.png)

Fill passanger informations. Click 'Continue'.
![onur-pic3](https://s10.postimg.org/8y9ra4vcp/image.png)

Click 'I don't want Qualified Ticket Program' radiobutton then click continue. It is possible to get ticket price from this page.
![onur-pic4](https://s10.postimg.org/g5bg6069l/image.png)

Fill credit card informations then click buy button. It is possible to get ticket price from this page.
![onur-pic5](https://s10.postimg.org/su5qpoce1/image.png)

Finally you should get an error massage like this. It means scraping process done successfully.
![onur-pic6](https://s10.postimg.org/4exiomdh5/image.png)
