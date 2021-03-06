# **Question/Need**
Prior to the COVID-19 pandemic there was a net influx of people moving to NYC. This influx was disrupted by lockdown and resulted in a decrease in rental prices and therefore, residential real estate prices. However, NYC is beginning to experience a reemergence due to vaccinations and reduced numbers of COVID-19 cases. Therefore, it is an opportune time for residential real estate developers to invest in previously burgeoning neighborhoods of NYC and nearby areas. Identification of pre-pandemic burgeoning neighborhoods can be facilitated by analyzing traffic through individual subway stations, with a focus on traffic more likely assosciated with commuters. 

# **Data**
The metropolitan transportation alliance (MTA) records data on entries on exits for each turnstile over the time period of 4 hrs. The MTA turnstile data is released on a weekly basis beginning from May 2010 to present and is available at https://www.wba.mta.info/developers/turnstile.html.  The features of the data include necessary information to ID each turnstile, entries and exits presented as cumulative data, and timestamps. 

To address the question described above, I focus on the data pre-pandemic - May 2010 to January 2020. I will begin by aggregating the data for each station. I will then focus on time frames that are most likely to indicate residential use - entries from 4 am to 12 pm and exits from 4 pm to 12 am on weekdays. These time frames are chosen because they are most likely to coincide with use of the subway system for commuting to work and returning home. Since the entry and exit data are cummulative, I will need to determine number of entries or exits by subtracting the timestamp of interest by the timestamp immediately prior. 

I want to identify areas around stations that have demonstrated a higher-than-average increase in commuter traffic, so I will compare the increase in commuter time entries and exits between all stations 

Based on my time living in NYC, I predict that stations that display the most increased commuter traffic will be primarily located in Brooklyn and Queens somewhere between 2-4 stops from Manhattan. 

# **Tools**
MTA turnstile data will be scraped using BeautifulSoup and processed into an SQL databse. The resulting database will then be queried using SQLAlchemy, and the appriopriate dataset will cleaned and analyzed using pandas. For data visualization, I will use matplotlib, seaborn, and plotly express.  


# **Minimal Viable Problem (MVP)**
As a MVP, I will begin by using a subset of the full dataset I plan to use above. One option would be to focus on a single month across all years available. Finally, I will map the results higher than average increase in commuter traffic onto a map of NYC. 

