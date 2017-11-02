# data-512-a2

#### Repo for DATA_512 Assignment 2
This file describes the requirements and steps needed to produce __[visualizations](https://github.com/mykebrowne/data-512-a2/blob/master/top10_proportion_plot.png)__ representing countries ranked in terms of: 

 - The number of English language Wikipedia politician articles per 1000 population 
 - The proportion of English language Wikipedia politician articles which are high quality, as predicted by the __[ORES](https://www.mediawiki.org/wiki/ORES)__ machine learning algorithm. 
 
 
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
- Population data is provided by __[Population Reference Bureau](http://www.prb.org/DataFinder/Topic/Rankings.aspx?ind=14)__.
- Data concerning __[English Wikipedia articles on politicians by country](https://figshare.com/articles/Untitled_Item/5513449)__ are licensed under CC-BY-SA 4.0.


#### API documentation for ORES 

The ORES (Objective Revision Evaluation Services) __[API](https://ores.wikimedia.org/v3/#/scoring)__ has an end-point which, for a given: <br> 

- Context (the name of the Wikipedia project, in this case 'enwiki' for English language Wikipedia)
- Revision id (the id given to the last edit of a particular Wikipedia article)
- Model (scoring model - in this context wp10)

returns a JSON object with a key-value pair "prediction" and one of six quality values. <br>  

For example: https://ores.wikimedia.org/v3/scores/enwiki/235107991/wp10 returns prediction:  "Stub" 


#### Data file 

The __[data file](https://github.com/mykebrowne/data-512-a2/blob/master/page_quality_population.csv)__ created as part of this project has the following columns: <br> 

- country (character) 
- article_name (character) - the name of the English language Wikipedia article  
- revision_id (integer) - the id given to the last edit of the Wikipedia article 
- article_quality (character) - the quality of the article as predicted by ORES 
- population (integer) - the Mid-2015 population of the country <br> 

Please note that this list only includes arcticles from countries which are listed in the __[Mid-2015 population](http://www.prb.org/DataFinder/Topic/Rankings.aspx?ind=14)__ file from the Population Reference Bureau __and__ which have predicted scores from ORES. 


#### Steps to reproduce analysis 

This __[Jupyter notebook](https://github.com/mykebrowne/data-512-a2/blob/master/hcds-a2-bias.ipynb)__ contains the steps and code needed to reproduce this analysis.  


#### Reflection: Bias in data 



