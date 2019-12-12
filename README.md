# burmese-python-project
Team 3 project

README.md
# Planning
retrieve the normal SQL dataset
retrieve iNaturalist dataset
# Github
We created the repo, - Elda in charge of the repo
create a single jupyter notebook for everyone to pull - named main.ipynb
Elda uploaded python.sql file
we will each maintain a README to consolidate at the end
we navigated to our path on our individual machines
We each used $ git clone <repo> using the following link: https://github.com/evill013/burmese-python-project
# Sequel Pro / MySQL Workbench
connected to SequelPro, imported python.sql
Added Database "burmese_python_project"
Ran query to create the table "pythons", 
Ran query to insert values
use burmese_python_project;
SELECT * from pythons LIMIT 1;
we infer that every row is a sighting
make sure to filter the SQL Location to lose the non-Florida sightings for our calculations
jupyter notebook to connect to the DB, 
which columns are we keeping? latitude, longitude, id(append gov), observed_on, 
# iNaturalist scraping/API/
identify the taxonomy number for the Burmese python
loop through all those pages
FLORIDA = placeid=21
TAXONID = 238252
# Directives from Client
Client would like to know, among other things:
Are sightings of Burmese pythons in the wild increasing? (Client wants an analysis with visualizations)
    lineplot over time showing frequency of sightings
Which three counties are most affected? (Analysis + visualization) 
    split on comma, create a new column for CountyName
    unique columns, count the sightings per CountyName, sort descending
Are there geographic hotspots? If so, what are the probabilities that volunteers will find pythons in those areas between today's date and Dec 31st? (Analysis + viz)
    Viz: big red circle on a map for frequency of sighting on a map (lat/long) - look up DJK's code for the boundary map he created
    Analysis: 
When are people most likely to spot pythons, and why? (Analysis + viz)
    Viz: frequency by observation date (OBSDATE)
    Analysis: research python activity - are they diurnal? do we have a timeseries for the observations? not in the official dataset, but maybe inaturalist
Are sightings cyclical? (Analysis + viz)
    Viz: TimeSeries Analysis
    Analysis: explanation
How many python observations do you predict will be recorded for the full 2019 year? (time-series analysis) 
    time-series - use it to predit a value(sum of 2019 sightings)
    
For purposes of developing a social media/citizen science campaign, the client would like to know:
    Should we be using iNaturalist to get the public more engaged?
        our answer
    Which iNaturalist users are most active in sighting pythons?
        groupby Users who have sighted Burmese Pythons, aggfunc to Count, further breakdown by other details?
    Which iNaturalist users are most active in identifying pythons? Hint: iNaturalist observations must be confirmed by other users... 
    Which iNaturalist users are most connected in the python-spotting community?
        Network Analysis - which users are iNaturalist friends with others? 
    Are any wildlife officials also using iNaturalist? (Hint: yes) (edited)
        figure out how to find these 