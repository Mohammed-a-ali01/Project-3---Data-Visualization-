# Project-3-Data-Visualization-Track
# Los Angeles County Crime Data

## Project Overview
For this track, your group will tell a story using data visualizations. Here are the specific requirements:

    Your project must include visualizations. The visualizations can be created with:

        Python (e.g. Matplotlib, Pandas plotting, hvplot)

        JavaScript (e.g. Plotly or Leaflet)

        A Python or JavaScript visualization library that was not covered in class

    Data must be stored in and extracted from at least one database (PostgreSQL, MongoDB, SQLite, etc).

    Your project must include at least one JavaScript OR Python library that we did not cover.

    Your project must be powered by a dataset with at least 100 records.

    Your project must include some level of user-driven interaction, such as:

        HTML menus, dropdowns, and/or textboxes to display JavaScript-powered visualizations

        Flask backend with interactive API routes that serve back Python or JavaScript created plots

        Visualizations created from user-selected filtered data, which could be powered by:

            JavaScript libraries

            Python in Jupyter Notebook

            Command-line Python scripts that save visualizations locally

        Remember: You have learned how to filter data in Pandas, JavaScript, SQL, SQLAlchemy, and MongoDB.

    If possible, your final visualization should ideally include at least three views.

    Your GitHub repo must include a README.md with an outline of the project including:

        An overview of the project and its purpose

        Instructions on how to use and interact with the project

        At least one paragraph summarizing efforts for ethical considerations made in the project

        References for the data source(s)

        References for any code used that is not your own



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


## Sources

### Data Set
Kaggle.com

### Zip codes geojson file
https://data.lacounty.gov/datasets/lacounty::la-county-zip-codes/about

## Team Members
- Yi Wen
- Daniel Molina Valencia
- Mohammed Ali
- Aditya Singh Thakur