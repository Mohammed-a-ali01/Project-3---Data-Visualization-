# Project-3-Data-Visualization-Track
# Los Angeles County Crime Data

## Project Overview

This project delves into the analysis and visualization of crime data in Los Angeles spanning from 2000 to May 2024, sourced and cleaned from a Kaggle dataset.
Excluding the year 2024, the analysis focuses on four key aspects:
1. Total and by type annual crime trends using line plots
2. Top 10 crime types per year depicted in a horizontal bar graph
3. Top 3 crime types per year distributed by Zip Codes through a choropleth map
4. Victim demographics in identity theft cases explored via treemaps.

Utilizing Python, Pandas, Matplotlib, Plotly, Dash, and SQLite, this analysis merges individual contributions into a cohesive group effort.
The aim is to uncover meaningful insights that inform strategic decisions in law enforcement, urban planning, and community safety across Los Angeles.
This approach underscores our commitment to leveraging data visualization for actionable intelligence and public benefit.

An overview of the project and its purpose
- the project is designed to study the rate of criminal actitives in the Los Angeles Area. The Los Angeles area is notorius already for its oraginzed gangs. With the precursor in mind we are choosing to look at the rate of criminal activiies post covid limited to a time span of one year. The project looks at crimes broken down by category, density and ethinicity.
We have created multiple visualization to closely look at the trends in different type of crimes and how they have affected the many ethinicites across the multiple nebghiourhood.
Problem Statement:
What is the problem? Who would be interested? And how will it help them?
- Problem: Hownmuch crime was being committed in LA
- People interested - Student of criminology , Police analyst , data anayisi enthusaist
The project would help them to beeter understand the dynamics of the are and attempt to lower crim and make LA safe.
Data Collection:
What are different data source types, size and shape of data
What are some challenges you faced with collection, if any
- some of the data file we encounterd were too large encompassing many years for data, some data sets were encomapssing a extremely large geographical aread . Long time line and area coverage tended to have extremely large file size.
Overall Approach:
How did you approach this project? Problem framing -> data exploration -> data cleaning -> data storage -> data visualization.. and so on
How much time you spent on each?
- we took a simple and systematic approach towards the project. we first identified a broad problem statement and narrowed it down further to isolate the problem further.  Reducing the area covered and time lines allowed us to explore and mitigate data sets that might not have been suitable due to many data points. The data set we used was relative sized and covered a small are so cleaning the data was straight forward. after cleaning and turning the data we broke down the visualizations into line and bar graph, tree map and heat maps.
Solution Architecture:
What is the end to end source to target data flow look like?[A database should be used to store data and retrieved from there to plot visualizations]
Which tools you used along the process to store, process and visualize data?
- jupyter notebook and dash
What are libraries/ tools you used that we didn't see in class, highlight them and wh

### Cleaning the data and sending it to a Sqlite.

- Removed colums not needed.
- Create the "Year" column by splitting the date and time from the "DATE OCC" column, and then extracting the year using Datetime library.
- Map the "Vict Descent" replacing the codes with the actual descents.
- Create the "Zip Code" column, using geopandas and shapely.geometry to transform the  "LON" and "LAT" data.
- Removed some other columns not needed and renamed the final columns for readability.
- The final Data Frame was sent to a sqlite data base using sqlite3.

### Querying our data base to create the visualizations using Plotly, Python Code, Pandas and Dash.

- The data base was query using sqlalchemy. In this query 2024 was filtered out, as it was partial.
- Create the Dash APP to show the three visalizations as a Dashboard.
- A dropdown menu is used to select the year the user wants to see.


## Ethical Considerations

In light of growing awareness of data ethics, several key considerations were observed while analyzing the Los Angeles crime dataset available.
- Firstly, the dataset's CC0 license allows for unrestricted use, including commercial purposes, without seeking permission from the author.
- Secondly, all data handling adhered to privacy regulations such as GDPR and CCPA to protect individuals' personally identifiable information.
- Thirdly, the analysis was conducted transparently, documenting data sources, methodology, and assumptions to facilitate understanding and validation of results.
- Lastly, the analysis was conducted with the purpose of enhancing students' data analytics skills while ensuring no harm to individuals or communities, thus aligning with ethical standards. These ethical practices not only ensure legal compliance but also foster trust and integrity in analytical outcomes.


## Sources

### Data Set
https://www.kaggle.com/datasets/middlehigh/los-angeles-crime-data-from-2000/data

### Zip codes geojson file
https://data.lacounty.gov/datasets/lacounty::la-county-zip-codes/about


## Team Members
- Yi Wen
- Daniel Molina Valencia
- Mohammed Ali
- Aditya Singh Thakur