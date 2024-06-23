# Project-3-Data-Visualization-Track
# Los Angeles County Crime Data

## Project Overview

This project integrates individual contributions into a cohesive group effort to analyze crime data in Los Angeles spanning from 2000 to 2023. Given Los Angeles' reputation for organized gangs and criminal activities, the aim is to uncover insights that can inform strategic decisions in law enforcement, urban planning, and community safety.

The findings are intended to be valuable for a range of stakeholders, including criminology students, police analysts, data analysis enthusiasts, and others interested in understanding urban crime dynamics.

The results aim to enhance understanding of the city's dynamics to potentially reduce crime rates and improve overall safety in Los Angeles.

Following the analysis, we have developed a dashboard featuring visualizations that highlight four key aspects:
    1. Annual trends in total and by crime type using line plots.
    2. The top 10 crime types per year presented in a horizontal bar graph.
    3. Distribution of the top 3 crime types per year across Zip Codes via a choropleth map.
    4. Detailed insights into identity theft, including victim demographics, visualized using a Tree Map.

## Instructions
- Clone the project repository to your local machine.
- Navigate to the cloned repository and create a "Resources" folder.
- Download the following files from: (https://drive.google.com/drive/folders/1SHJT23DdEPBBs0kaS0cqE71lcLufb2ha):
    - Crime_Data_from_2020_to_Present.csv
    - LA_County_ZIP_Codes.geojson
- Save the files inside the "Resources" folder.
- Open and execute the code file clean_code.ipynb using Jupyter Notebook.
- Open your web browser and navigate to http://127.0.0.1:8050/ to access the Dash application.

## General steps followed
- Created a Jupyter Notebook and imported data set
- Cleaned the data and created a clean pandas Data frame that was extracted into a SQlite data base
- Queried the data base to obtain the data needed for the analysis and visualizations
- Prepared data needed for the visualizations
- Created the Dash application and coded each one of the visualizations.

## Detailed steps
1. Imported Dependencies

2. Cleaned the data and created Data Base.

    - Imported csv file using *Pathlib* and *Pandas* libraries.
    - Removed columns not needed.
    - Created the "Year" column by splitting the date and time from the "DATE OCC" column, and then extracting the year.
    - Mapped the "Vict Descent" replacing the codes with the actual descents.
    - Created the "Zip Code" column using *Geopandas* and *Shapely.geometry* libraries and the geojson file containing the zip code coordinates to obtain the zip codes from the "LON" and "LAT" columns.
    - Removed some other columns not needed and renamed the final columns for readability.
    - Extracted the final Data Frame to a SQlite data base using *SQlite3*.

3. Queried Data Base, and created dashboard and visualizations.
    - Queried the Data Base using *sqlalchemy* to create a base Data Frame with *Pandas*. 2024 data and records with no zip code were excluded.
    - Created a zip code Data Frame needed for the Choropleth map
    - Created lists needed for the dropdown menus.
    - Simplified the geojson file limiting it to the zip codes needed, reducing its precision and simplifying the geometries.
    - Created the Dashboard with *Dash*.
    - Defined the Layout
    - Defined callback and function to create a Total Trend Line and a Crime Type Trend Line using *plotly*. The Crime Type Trend line changes based on the type of crime selected. 
    - Defined callback and function to determine the radio button options and to build the Bar chart using *plotly express*. The Bar Chart updates based on year selected.
    - Defined callback and function to produce a Choropleth Map using *plotly graph_objects*. The map changes based on the year and type of crime selected.
    - Defined a callback and function to create the Tree Map using *plotly graph_objects* that updates based on a separate year dropdown selection.

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