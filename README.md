# Views on English Wikipedia

## Goal of the Project 
The goal of this assignment is to construct, analyze, and publish a dataset of monthly traffic on English Wikipedia from January 1 2008 through September 30 2017.Combine data Wikipedia traffic from two different Wikimedia REST API endpoints into a single dataset, perform some simple data processing steps on the data, and then analyze that data.

## License and Terms
[MIT License](https://opensource.org/licenses/MIT)

Wikimedia's [general Terms of Use](https://wikimediafoundation.org/wiki/Terms_of_Use/en) and [Privacy Policy](https://wikimediafoundation.org/wiki/Privacy_policy).

## Relevant API
The legacy Pagecounts API ([documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts), [endpoint](https://wikimedia.org/api/rest_v1/#!/Pagecounts_data_%28legacy%29/get_metrics_legacy_pagecounts_aggregate_project_access_site_granularity_start_end)) provides access to desktop and mobile traffic data from January 2008 through July 2016.

The Pageviews API ([documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews), [endpoint](https://wikimedia.org/api/rest_v1/#!/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end)) provides access to desktop, mobile web, and mobile app traffic data from July 2015 through September 2017.

## Final Data File

Final data saves in ```en-wikipedia_traffic_200801-201709.csv```

Values shown as follows:

|  Column | Value  |
|---|---|
| year  |  YYYY |
|  month |  MM |
|  pagecount_all_views |  nums_views | 
|  pagecount_desktop_views |  nums_views |
|  pagecount_mobile_views | nums_views  |
|  pageview_all_views |  nums_views |
|  pageview_desktop_views |  nums_views |
|  pageview_mobile_views | nums_views  |

Data for pageview  come from Pageviews APT are called pageviews_desktop_201507-201709.json, pageviews_mobile-app_201507-201709.json and pageviews_mobile-web_201507-201709.json.
pageview_all_views is all views for desktop, mobile-app, and mobile-web.
pageview_desktop_views is views for desktop
pageview_mobile_views is views for both mobile-app and mobile-web views.

Data for pagecount come from legacy Pagecounts API are named as pagecounts_desktop-site_200801-201607.json and pagecounts_mobile-site_200801-201607.json.
pagecount_all_views is all views for desktop and mobile views.
pagecount_desktop_views is desktop-site views.
pagecount_mobile_views is mobile-site views.


## Directory Structure
```
data-512-a1 (master)
|
|     License
|     README.md
|     en-wikipedia_traffic_200801-201709.csv
|     hcds-a1-data-curation.ipynb
|     views of english wikipedia.jpg
|	    

```

## Important Notes

Since a new pageview definitin took effect on May 2015, data from the Pageview API excludes spiders/crawlers, while data from the Pagecounts API does not
