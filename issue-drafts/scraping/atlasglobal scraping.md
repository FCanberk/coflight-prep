# TODO: canberk - describe the issue

Please refer to [Scraping Guide](https://github.com/FCanberk/coflight-prep/blob/master/guides/scraping%20guide.md) first to see the technologies used and the input / output formats.

Every 5 minutes [AtlasGlobal](https://www.atlasglb.com/) website will be visited and every flight listed in the dataset will be scraped. The output will be sent to orchestrator.

A valid citizenship id number and a valid credit card number will be needed for scrapping. Citizenship id numbers could be generated [here](https://www.simlict.com/tcno.html) and credit card numbers could be generated [here](https://names.igopaygo.com/credit-card).

These are the steps that should be followed:

**Areas in the circle must be clicked or filled. Areas in rectangle have information to gather.**

Select departure airport, arrival airport, departure date, one way/round trip and if it is round trip select return date.
![atlas-pic1](https://s23.postimg.org/6ji8y24ln/at1.png)

Select departure time in available flights. Get the flight date&time. If it will be one way flight click 'Continue'. It is possible to get ticket price from this page.
![atlas-pic2](https://s10.postimg.org/wuqcfluop/at2.png)

If it will be one way trip skip this step, otherwise, select return flight. It is possible to get ticket price from this page.
![atlas-pic2.5](https://s2.postimg.org/9hzg9xcqx/at2_2.png)

Fill passanger informations. Click 'Continue'. It is possible to get ticket price from this page.
![atlas-pic3](https://s23.postimg.org/f31mvtcy3/at3.png)

Click 'PROCEED TO CREDIT CARD PAYMENT'. It is possible to get ticket price from this page.
![atlas-pic4](https://s23.postimg.org/w64erbtmz/at4.png)

Click 'CREDIT CARD STANDART PAYMENT' radio button. Fill credit card informations. Click 'I'm not interested' radio button, check 'I Accept the Agreement'then click 'Approve Payment'.
![atlas-pic5](https://s23.postimg.org/eu425w05n/at5.png)

Finally you should get an error massage like this. It means scraping process done successfully.
![atlas-pic6](https://s23.postimg.org/az0o3bgzv/at6.png)
