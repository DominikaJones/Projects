## Problem Statement
Amongst all the craziness of 2020, the one thing we did not expect to focus on was the Black Lives Matter movement. It has been 157 years since slavery was abolished and 150 years since people of color received the right to vote. Unfortunately, systemic racism continues in the United States and other countries around the world. We at Equality, work with law enforcement to teach racial bias. We do this by evaluating the crime in your area and looking at the number of fatal encounters. With our help, we can reduce your number of racially biased fatal encounters.
In order to solve our problem statement, our team will use a dataset documenting the fatal encounters nationwide with police from 2000 to 2020. We will look to build a model that can predict race, and in doing so, see if racial bias plays a factor in these deaths. Further, we would look to find the locations where this racial bias is most prevalant, and look to change cultures within the police departments at these different locations. 

## Executive Summary
[Executive Summary](..assets/Executive Summary.txt/)

## The Data
The data was collected from fatalencounters.org. It comprised of descriptive features of each deadly encounter with police over the past 20 years, including name, gender, age, location information, agenecies involved, cause of death, intended use of force, race, a brief description, and in most cases, the race of the victim. In the cleaning process, we decided to keep 8 features. One main concern we had was that race was unspecified in over 8000 cases. We address this later in our modeling. A column of 'race with imputations' was dropped, as we decided to be sure of race so that we did not train a model on information we were not confident with. The uncleaned and cleaned dataset can be found in the repo. 

## Contents: 

1. Code Folder 
    - Part 1: Data Scrapping
    - Part 2: EDA
    - Part 3: Modeling
2. Data Folder
    - fatal_encounters.csv
    - fatal_encounters_eda.csv
3. Assets Folder
    - presentation pdf
    - images

## Cleaned Data Dictionary 
|Feature|Type|Dataset|Description|
|---|---|---|---|
|Age|int|fatal_encounters| Age of person in encounter | 
|Latitude|float||fatal_encounters| Latitude of encounter
|Longitude|float|fatal_encounters| Longitude of encounter
|Gender|int|fatal_encounters|Binarized gender of person involved in encounter
|State|int|fatal_encounters|Dummified variables based on the State the encounter took place in
|Cause of Death|str|fatal_encounters|Cause of death in encounter
|Intended Use of Force|str|fatal_encounters|Intended use of police force
|Race|str|fatal_encounters|Race of person in encounter (target variable)

## Resources
    - https://www.census.gov/quickfacts/fact/table/US/PST045219
    - https://libguides.princeton.edu/c.php?g=598338&p=4142165
    - https://www.nytimes.com/interactive/2020/07/03/us/george-floyd-protests-crowd-size.html
    
## Software requirements
Our project primarily used pandas to load, clean, and manage the large dataset. Other packages include numpy, seaborn, matplotlib, scikit-learn and folium for the heatmap visual. 