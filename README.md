# data-512-a2

#### Repo for DATA_512 Assignment 2
This file describes the requirements and steps needed to produce a __[time series visualization](https://github.com/mykebrowne/data-512-a1/blob/master/wikipedia_traffic.png)__ of Engish Wikipedia traffic, split by mobile and desktop sites during January 2008 to September 2017, using Jupyter notebook and the Wikimedia Rest API. 


#### Software requirements 

- __[Jupyter notebook](http://jupyter.org/about.html)__ running an R kernel.  
- This can be done locally by __[installing](http://jupyter.org/install.html)__ Juypter notebook or, alternatively, on the Jupyter server. 
- If done locally, Python is a requirement (Python 3.3 or greater, or Python 2.7) for installing Jupyter. 


#### Licensing 

- Jupyter/jupyter is licensed under the __[BSD 3-clause "New" or "Revised" License](https://github.com/jupyter/jupyter/blob/master/LICENSE)__. 
- R as a package is licensed under GPL-2 | GPL-3. 
- Python 2.2 and above are licensed as per https://docs.python.org/3/license.html
- Content accessed through the __[Wikimedia Rest API](https://en.wikipedia.org/api/rest_v1/)__ is licensed under the CC-BY-SA 3.0 and GFDL licenses. 
- Use of the Wikimedia Rest API is under the __[Wikimedia Terms of Use](https://wikimediafoundation.org/wiki/Terms_of_Use/en)__.


#### API documentation

The Wikimedia Rest API has two endpoints for Wikipedia traffic:  
- The __[Pagecounts API](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts)__ which provides access to desktop and mobile traffic data from January 2008 to July 2016. 
- The __[Pageviews API](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews)__ which provides acesss to desktop, mobile web and mobile app traffic data from July 2015 to present. 


#### Data file 

The __[data file](https://github.com/mykebrowne/data-512-a1/blob/master/en-wikipedia_traffic_200801_201709.csv)__ created as part of this project has the following structure: 

- year (integer) - the year to which the traffic relates  {2008, 2009, ... 2017}. 
- month (integer) - the month to which the traffic relates  {1, 2, ... 12}. 
- pagecount_all_views - the total number of views (English desktop and mobile sites) as defined by the Pagecounts API.
- pagecount_desktop_views - the total number of views for the English desktop site as defined by the Pagecounts API. 
- pagecount_mobile_views - the total number of views for the English mobile site as defined by the Pagecounts API. 
- pageview_all_views - the total number of views (English desktop and mobile sites) as defined by the Pageviews API.
- pageview_desktop_views - the total number of views for the English desktop site as defined by the Pageviews API. 
- pageview_mobile_views - the total number of views for the English mobile site as defined by the Pageviews API. 

Please note that views from the Pagecounts API includes views from non-human agents (e.g. spiders and webcrawlers).  Views from the Pageviews API has been filtered to exclude views from non-human agents.  


#### Steps to reproduce analysis 

This __[Jupyter notebook](https://github.com/mykebrowne/data-512-a1/blob/master/hcds-a1-data-curation.ipynb)__ contains the steps and code needed to reproduce this analysis.  
