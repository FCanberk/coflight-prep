## High Level Design Overview

Below are the modules in the project.

- Scrapers
- Orchestrators
- Scraping Gateway
- Reporting Web Server
- Reporting App Server
- Database

### Scrapers

bla bla bla

### Orchestrator

bla bla bla

### Scraping Gateway

bla bla bla

### Reporting Web Server

Scraped information will be made available for the users. They will be able to query the information gathered with the project. The reporting web server will be providing the web functionality.

### Reporting App Server

This module is to provide an interface to the database for inserting and querying scrap data. It will be used by the web server to retrieve information requested by the users in browsers and the persistence requests from `Scraping Gateway`

### Database

All operational data will be stored in a document db (most likely MongoDB). Operational data includes the periodic scraping of tickets, scraping metadata (destination, flight date and time, etc)
