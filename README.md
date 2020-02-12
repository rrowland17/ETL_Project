# ETL_project


# Data sources: 
We decided to use BeautifulSoup to scrape the URLs that were set up in HTML to get the passing, receiving, and rushing stats for all 130 NCAA teams. 
```
https://www.espn.com/college-football/teams
```

# What transformations:
The HTML string itself was set up pretty clearly and fairly easy to parse. Using a four loop, we were able to import the individual team URLs into a Pandas Dataframe. From there, we were able to clean up the multiple statistical tables into three clean dataframes: passing, rushing, and receiving. We then imported those data frames into a dictionary, converting the dataframes into JSON strings that were ready to be uploaded.

# Where is data loaded: 
We chose to load our information into MongoDB because we wanted to avoid creating schemas and we had uniform tables which made it easy to upload without having to worry about primary keys. The final collection has the passing, rushing, and receiving statistics saved as JSON strings for 130 NCAA teams. 
