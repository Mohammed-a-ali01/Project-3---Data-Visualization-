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