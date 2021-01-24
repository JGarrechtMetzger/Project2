# Project 2: \"How to Help Craigs List Their Instruments\""

# Description
* Scrape post information from Craigslist.org in the San Francisco Bay Area region - Musical Instruments section.  The goal is to predict what features (attributes of posts) predict advertised sale price (in USD).

# Target & Feature Variables

**Target**:
* *Price*
    * Advertised price listed on search page results
    * Integer
    * Units: USD
    
**Features**:
* *has_pics*
    * Is there at least one picture in the posted ad?
    * Units: Scraped as boolean; converted to 0 & 1 in dataframe
        
* *title_char_count*
    - How long is the title of the posted ad?
    - Units: Number of characters
* *day*
    - What day of the month is the ad posted?
    - Integer representing calendar day (e.g., January 5th, 2021 is represented by '17')
* *hours*
    - What time of day was the ad posted?
    - Integer (1-24)
    - Units: hours in military time.  Hour is binned by the time in hh:mm.  Example, 15:01 and 15:59 both return '15'
* *hood*
    - What is the location tagged to the posted ad?
    - Scraped at the 'neighborhood' scale (defined by Craigslist) from a dropdown list of neighborhoods.  Users could also chose to fill in their own location choice.  This resulted in >200 different neighborhoods from my scraping.  Because of time constraints, this feature was not included in the analysis for Project 2.  Future work can utilize Craiglist regional breakdown where the SF Bay Area is split into only 6 regions.  One hot encoding can then be applied to this location data.

# Data Used

* html scraped from craigslist.org
* Future work can include 2020 census data

# Tools Used

* Python
* scikit-learn
* NumPy
* seaborn
* Google Chrome
* BeautifulSoup
* pandas
* matplotlib
* Adobe Illustrator

# Possible Impacts of My Project

This project can be used to understand what features a Craigslist ad posting may be predictive of the posted instrument sale price in the San Francisco Bay Area.  The feature testing of different ad attributes (e.g., time of post, location of post, length of post title) will help Craigslist users identify which attributes are most associated with ads with higher posted sale prices.  This is turn may be used to help guide users' own advertisement construction and implementation.  For example, if different neighborhood tags from the same geographic area (e.g., \"Oakland\" vs. \"94952\") predict different prices for the same item type, it may be beneficial to chose the location designation associated with higher posting price. This project will also help identify ad attributes that do not predict higher posted prices.  Initial results suggest that length of title, day of the week, and the inclusion of a picture do not predict higher posting price although more data needs to be collected to thoroughly explore this relationship.

Future work may investigate granular geographic using the upcoming US Census data. 
