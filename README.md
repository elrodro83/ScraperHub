# ScraperHub

An alternative to [Kodi](http://kodi.tv/)'s Universal Scrapers for artists, albums, music videos and movies.

## Overview

The idea is to have a centralized remote application that queries the different data source sites, aggregates the information from the different sites and returns everything required by the media center.

Having this remote application avoids a big limitation on Kodi scrapers that is that all processing must be done with regular expressions. This remote application, powered by [Mule](https://github.com/mulesoft/mule), uses accurate tools for parsing the data from the sites (json, XML and HTML). Read [here](http://stackoverflow.com/questions/1732348/regex-match-open-tags-except-xhtml-self-contained-tags/1732454#1732454) to know why changing this would be good.

A single application to scrape all types of data would allow to implement some features are are near impossible to implement currently using Kodi alone:

* __Fetch data from many sites simultaneously.__ This will reduce the total time used to scrape a whole collection.
* __Properly scrape music concerts.__ Currently, the only way to scrape concert videos (like dvd releases of a live album, for instance) is to add them like movies. This new scraper will allow to aggregate the movie data with the music (artist and release) in order to add them to the music library instead of the movies one.
