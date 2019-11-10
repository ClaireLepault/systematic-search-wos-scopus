# systematic-search-wos-scopus
This repository contains notebooks and data for the short presentation "Systematic search on Web of Science and Scopus", given in November 2019. It takes place in the preparation of the 6th Assessment Report of IPCC Group III and introduces the basics of creating a search equation, exporting the associated results from Web of Science (WoS) and Scopus and merging all the results into a single database. The search and visualization of the years of projection and distribution of the country studies are finally given. <br>

The tutorial is intended for beginners in Python but the functions are not studied in detail and it may be necessary to search more explanation on the documentation of the libraries used. Furthermore, to carry out searches on WoS and Scopus, it is necessary to have institutional identifiers because their databases are not openaccess.

### Content

There are three associated IPython notebooks:

* [1_Search_equation](1_Search_equation.ipynb): Provides a basic introduction to general search rules on Web of Science and Scopus and tips for creating complex research equations with Python (for example on countries or years).

* [2_Export](2_Export.ipynb): Covers the application of advanced search on Web of Science and Scopus and proposes a method for storing and merging databases resulting respectively from the websites.

* [3_First_processing](3_First_processing.ipynb): Includes the merge of Scopus and Web of Science databases and some text mining on titles, abstracts and authors keywords to visualize years of projection and coutries studies inside the final database. To access online the graphs, you can use the nbviewer from Jupyter on this [page](https://nbviewer.jupyter.org/github/ClaireLepault/systematic-search-wos-scopus/blob/master/3_First_processing.ipynb) because Github doesn’t show interactive graphs as these ones created with the plotly library

To applicate the systematic search techniques, the following equations have been used on November 6th, 2019: 

* On WoS : <br>
  * TS = (("environment" OR "enabling condition*") AND ("greenhouse gas reduct*" OR decarboni?ation OR "climate change mitigation"))

* On Scopus : <br>
  * TITLE-ABS-KEY ( ( "environment" OR "enabling condition*" ) AND ( "greenhouse gas reduct*" OR decarboni?ation OR "climate change mitigation" ) )

The corresponding records are in the [Exported](Exported) folder.

The final database is also available [here](final_database.xlsx) in Excel format.

### Dependencies

This code has been tested with Python 3.7. The core package requirements are:

* pandas

* numpy 

* joblib

* plotly (tested with v4.2.1)
