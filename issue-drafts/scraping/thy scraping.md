# TODO: canberk - describe the issue

Please refer to [Scraping Guide](https://github.com/FCanberk/coflight-prep/blob/master/guides/scraping%20guide.md) first to see the technologies used and the input / output formats.

Every 5 minutes [Turkish Airlines](http://www.turkishairlines.com/tr-tr/) website will be visited and every flight listed [here](FlightListLink) will be scraped. The output will be sent to orchestrator.

A valid citizenship id number and a valid credit card number will be needed for scrapping. Citizenship id numbers could be generated [here](https://www.simlict.com/tcno.html) and credit card numbers could be generated [here](https://names.igopaygo.com/credit-card).

These are the steps should be followed during one scraping session:
Areas in the circle must be clicked or filled. Areas in rectangle have information to gather.

Select departure airport, arrival airport, departure date, one way/round trip and if it is round trip select return date.
![thy-pic1](https://s23.postimg.org/c7nmm85xn/image.png)

Select the flight in available flights. Get departure date&time. It is possible to get ticket price from this page.
![thy-pic2](https://s12.postimg.org/eew04iral/image.png)

If it will be one way trip skip this step, otherwise, select return flight. It is possible to get ticket price from this page.
![thy-pic2.5](https://s12.postimg.org/4gb1i1hv1/a2_5.png)

Fill passanger informations then click 'Next'. It is not necessary to check 'Please remember data for my next bookings' button. 
![thy-pic3](https://s23.postimg.org/u1j4niozv/image.png)

Fill 'CardHolder's Personal Information'. Click 'Credit Card' radio button. Fill credit card informations. Click 
![thy-pic4](https://s21.postimg.org/avkofma2v/image.png)

Check 'I accept the Terms and Conditions' then click 'Next'.
![thy-pic44](https://s21.postimg.org/rxdihpoxz/a4_4.png)

Finally you should get an error massage like this. It means scraping process done successfully.
![thy-pic5](https://s23.postimg.org/6ol3508wb/image.png)
