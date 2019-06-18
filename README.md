# Pathways - the UNSW course handbook done right
---------------------------------------------

## Motivation

Pathways is a web app that lets you view details about UNSW courses, including timetables, prerequisites and course summaries, in a friendlier manner than the [course handbook](http://www.handbook.unsw.edu.au) and [timetable](http://www.timetable.unsw.edu.au) sites.

## Getting Started

It currently has the following components:

* **scraper.py** - A python script that scrapes the HTML from every course page on the legacy 2018 handbook
* **binder.py** - A python script that parses the downloaded HTML from the scraper and converts it all into a SQLite3 database
* **server.py** - The Python Flask Web App that interfaces with the SQLite3 database
* **static/index.html, static/css/main.css, static/js/main.js**, all the front end stuff, making heavy use of Bootstrap and jquery

### Prerequisites

* Python3 + pip3

### Running locally

* Run ```scraper.py``` then ```binder.py``` then ```server.py```
    * Note that ```scraper.py``` downloads ~130MB of data, which is then compress into a 6MB SQLite3 DB

Pathways is made available under the Apache License 2.0. Portions of the timetable display code are based on [Octangles](https://github.com/oliver-c/octangles).
