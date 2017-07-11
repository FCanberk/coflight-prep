Pegasus Airlines scraper needs formatted input to querying flights. This input will be in CSV format. It should include

* Departure airport code
* Arrival airport code
* Departure date and time
* Return date and time 
* One way/roundtrip info
* Cookie info values

informations in written order.

There should be three queries for each flight. First query should be **with** cookies, second should be **without** cookies then the third one should be **with** cookies again.

There should be 15 international and 15 domestic flights.

### Example 

`IST,MLX,20170928-1530,,OW,WC`<br>
`IST,MLX,20170928-1530,,OW,W0C`<br>
`IST,MLX,20170928-1530,,OW,WC`<br>
`IST,BEG,20170528-0600,,OW,WC`<br>
`IST,BEG,20170528-0600,,OW,WOC`<br>
`IST,BEG,20170528-0600,,OW,WC`<br>
`SKP,ESB,20171007-1200,20171014-2250,RT,WC`<br>
`SKP,ESB,20171007-1200,20171014-2250,RT,WOC`<br>
`SKP,ESB,20171007-1200,20171014-2250,RT,WC`<br>
`IST,ADA,20170101-0820,,OW,WC`<br>
`IST,ADA,20170101-0820,,OW,WOC`<br>
`IST,ADA,20170101-0820,,OW,WC`<br>

In this example there are four flights. Two of them are international and two of them are domestic flights.