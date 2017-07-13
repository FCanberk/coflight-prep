## High Level Design Overview

Below are the modules in the project.

- Scrapers
- Orchestrator
- Reporting Web Server
- Reporting App Server
- Database

### Scrapers

This module is to gather flight information from the airline companies. There will be four scrapers for four airline companies and each scraper will gather flight information with and without cookies. Flight queries will be made according to input format and output will be generated formatted. Input and output format specified in [scraping guide](https://github.com/FCanberk/coflight-prep/blob/master/guides/scraping%20guide.md).

### Orchestrator

This module is to organize and communicate with other modules. It sets the input value for `Scrapers` and gets the output value from scrapers. If the output is legit it stores the data via `App Server` in the `Database`.

### Reporting Web Server

Scraped information will be made available for the users. They will be able to query the information gathered with the project. The reporting web server will be providing the web functionality.

### Reporting App Server

This module is to provide an interface to the database for inserting and querying scrap data. It will be used by the web server to retrieve information requested by the users in browsers and the persistence requests from `Orchestrator`

### Database

All operational data will be stored in a document db (most likely PostgreSQL). Operational data includes the periodic scraping of tickets, scraping metadata (destination, flight date and time, etc)
