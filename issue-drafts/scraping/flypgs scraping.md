# TODO: canberk - describe the issue

Please refer to [Scraping Guide](https://github.com/FCanberk/coflight-prep/blob/master/guides/scraping%20guide.md) first to see the technologies used and the input / output formats.

Every 5 minutes [Pegasus Airlines](https://www.flypgs.com/) website will be visited and every flight listed in the dataset will be scraped. The output will be sent to orchestrator.

A valid citizenship id number and a valid credit card number will be needed for scrapping. Citizenship id numbers could be generated [here](https://www.simlict.com/tcno.html) and credit card numbers could be generated [here](https://names.igopaygo.com/credit-card).

These are the steps that should be followed:

**Areas in the circle must be clicked or filled. Areas in rectangle have information to gather.**

Select departure airport, arrival airport, departure date, one way/round trip and if it is round trip select return date.
![pgs-pic1](https://s11.postimg.org/wv7prob4j/pgs1.png)

Select departure time in available flights. Get the flight date&time. If it will be one way flight click 'Continue'. It is possible to get ticket price from this page.
![pgs-pic2](https://s2.postimg.org/ch036b155/pgs2.png)

If it will be one way trip skip this step, otherwise, select return flight. It is possible to get ticket price from this page.
![pgs-pic2.5](https://s18.postimg.org/6uswiyuyx/pgs2.5.png)

Click 'Continue with Current Choices'.
![pgs-pic3](https://s11.postimg.org/viq0psdoz/pgs3.png)

For Basic ticket select 'No baggage', otherwise, select 'Increase your baggage' from dropdown menu. Click 'Continue without Pegasus Plus login'. It is possible to get ticket price from this page.
![pgs-pic4](https://s11.postimg.org/rnr80yjwz/pgs4.png)

Click 'Continue'.
![pgs-pic5](https://s11.postimg.org/j6rpq1f83/pgs5.png)

Fill passanger informations. Click 'Continue to Payment'.
![pgs-pic6](https://s11.postimg.org/vmofjs8k3/pgs6.png)

Click 'Pay by Credit Card (Visa/MasterCard/Amex Garanti Cards)' and fill credit card informations. Check 'I have read the terms and conditions' then click 'Buy Now'.
![pgs-pic7](https://s18.postimg.org/v2qwkkkvd/Pgs7.png)

Click 'OK' or hit enter.
![pgs-pic7](https://s18.postimg.org/6niojilyh/pgs8.png)

Finally you should get an error massage like this. It means scraping process done successfully.
![pgs-pic8](https://s9.postimg.org/5snju1omn/pgs9.png)