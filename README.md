# data-512-a1

## Project Goal

The goal of this project is to recreate the original chart (shown below) using calls to the Legacy Pagecounts and Pageviews APIs. The accompanying Jupyter notebook details all the steps taken to output the chart. This is designed to be an exercise in reproducibility. Users should be able to run the cells in the Jupyter notebook and identically collecte, process, and analyze the English Wikipedia data.

! https://wiki.communitydata.cc/File:En-wikipedia_traffic_200801-201709_thompson.png


## License
The Wikipedia source data has a CC BY-SA 3.0 license. The details of this license are available here: https://creativecommons.org/licenses/by-sa/3.0/

Users can also refer to the Wikipedia Foundation REST API terms of use here: https://www.mediawiki.org/wiki/REST_API#Terms_and_conditions

## API Documentation

The APIs used to collect the data are documented below:

* Legacy Pagecounts: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts
* Pageviews: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews

## Processed Data

The accompanying csv file contains data in the format and columns listed below.

|Column | Value |
|-------|-------|
|year   |	YYYY|
|month	| MM|
|pagecount_all_views|	num_views|
|pagecount_desktop_views|	num_views|
|pagecount_mobile_views|	num_views|
|pageview_all_views|	num_views|
|pageview_desktop_views	|num_views|
|pageview_mobile_views|	num_views|

## Additional Information

The key difference between the APIs is that Legacy Pagecount could not discern web crawler traffic from user views. This feature was updated with the Pageviews API which was introduced in July 2015. Additionally, mobile views from the Pageviews API were calculated as the sum of mobile web and mobile app views. 