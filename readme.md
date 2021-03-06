## Crime Over Time Capstone Project

This project utilizes the FBI's Crime Data Explorer API, which is free to the public, and contains data from most Law Enforcement Agencies in the United States in the NIBRS format. NIBRS stands for National Incident-Based Recording System, which contains data on the offender during an incident, as well as their motivations used, the weapons used, relations to other types of offenses, and the victims demographic data by  location and by year. 

The home page allows you to select the information and location you would like to know about. Information can be about the Offense itself, and at a National Level and State Level. Upon submitting your query, the reports page will be loaded. On the reports page, will be a heatmap of the United States.

For the maps, I used the leaflet and mapbox (upon which leaflet is dependent), which were very easy to work with. For the graphs, I used the c3 and d3 (again, a c3 dependency) which were very simple as well, and I would recommend to anyone who is looking to place interactive graphs on their website. In order to limit my API requests, I used the requests-cache package for python, and an SQLite database, and matched the expiry time with the rate at which data is updated in the CDE database. PostgreSQL would have been used for the user/favorites functionality, and the skeleton is there, although it is nonfunctional. 

**Functionality**
- Able to load a heat map based on crime frequency in the last year for any crime in the CDE API.
- Form Fields change dynamically to automatically have the right criteria for the following fields.
- Offense Data is sorted into a pie chart for the most recent year and the requested state. 

**Missing Functionality that was Originally Planned**
- Able to load Victims demographic data on the heat map and graph. (half there)
- Data exportable as excel or csv. (not started)
- Categories with no data are excluded from form drop-downs or explained on the page. (not started)
- The pie chart lumps small data into an 'other' category to be more easily read. (not started)
- Graph and heat map can be adjusted with a time slider to load historical data. ( This is the original inspiration for the "Crime Over Time" Title. (not started)
- Accounts can be made to save your favorite queries. (half there)
- Verbal cues for UX (not started)
- A good title for each graph (half there)
- Agency Level data (half there)
- TESTING, no tests were written

**Bugs**
- The "variable" form field fails when on the results page

*If I were to do this project again:* 
I would list the features of the website and organize them in groups which can easily be implemented together, and tiers of priority. This way I would have been able to work in levels of priority, and had a presentable, complete product at each stage, although with less features. This way there would be no incomplete, half built, or untested features on the page, like the login feature.

I would also have written the Readme file at the beginning so that I could use it to keep track of what has been done and what is left to do. The readme could be used to maintain the organizational structure detailed above, and be used to follow along with the changes in each commit.
**