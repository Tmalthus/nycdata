# nycdata  

A mapping project to explore correlations between NYPD arrests and population density, food insecurity, and unemployment.  

Tools used include Python, QGIS, and GeoDa.  

## Data Sources  

NYPD historic arrest records, 2006 - 2024  
https://data.cityofnewyork.us/Public-Safety/NYPD-Arrests-Data-Historic-/8h9b-rp9u/about_data  

limited to arrest records between 2021 and 2024, inclusive

2020 Census Tracts  
https://data.cityofnewyork.us/City-Government/2020-Census-Tracts/63ge-mke6/about_data  

American Community Survey 5 year population estimates  
B01003: Total Population, estimates for all New York census tracts  
https://data.census.gov/table/ACSDT5Y2023.B01003?q=B01003:+Total+Population&g=040XX00US36$0500000,36$1400000  

Census Demographics at NTA level 2010  
https://data.cityofnewyork.us/City-Government/Census-Demographics-at-the-Neighborhood-Tabulation/rnsn-acs2/about_data  

NTA (Neighbourhood Tabulation Areas) polygons in geojson, 2010 and 2020 definitions  
https://www.nyc.gov/content/planning/pages/resources/datasets/neighborhood-tabulation  

Equivalence keys linking 2020 Census Tracts to 2020 NTAs  
https://data.cityofnewyork.us/City-Government/2020-Census-Tracts-to-2020-NTAs-and-CDTAs-Equivale/hm78-6dwm/about_data  

Emergency Food Supply Gap  
Unmet food need and estimates of vulnerable, food insecure, and unemployed populations  
https://data.cityofnewyork.us/City-Government/Emergency-Food-Supply-Gap/4kc9-zrs2/about_data  
 

## 2020 Population Density on 2020 census tracts  
<img width="2928" height="1926" alt="Image" src="https://github.com/Tmalthus/nycdata/blob/main/census_2020_pop_dens.png" />  

Many areas in New York have high population density, especially the boroughs of Manhattan, Brooklyn, The Bronx, and the central portion of Queens.  

My expectation is that arrests would be highest in areas of the highest population density, assuming that some rate of all people would commit crimes, so more police enforcement and arrests would follow in areas with more people.  

## Arrest Density on 2020 census tracts  
<img width="2928" height="1926" alt="Image" src="https://github.com/Tmalthus/nycdata/blob/main/census_2020_arrest_dens.png" />  

In this map of arrest density we see that many areas which have high population density also have high density of arrest records. This somewhat follows my expectation.  
However some areas of high population density have low arrest rates, like the southern parts of Brooklyn, and western parts of Queens. There are also areas with low population density and high arrest rates, particularly south west of Central Park.  

## Scatter plot of Population Density on Arrest Density
<img width="2544" height="1378" alt="Image" src="https://github.com/Tmalthus/nycdata/blob/main/census_2020_dens_scatter.png" />  

This scatter plot shows the relationship between population density and arrest density. A correlation of 0.258 shows a weak positive relationship between pop density and arrest density. My expectation was incorrect, arrest rates are not tied strongly to population density. Most census tracts, across a wide range of population densities, have low arrest rates.   

## High Low Cluster Map of Population and Arrest Densities  
<img width="2600" height="1472" alt="Image" src="https://github.com/Tmalthus/nycdata/blob/main/census_2020_dens_BiLISA_cluster_pop_arrest.png" />  

This plot shows clusters of tracts with high-high, low-low, low-high, and high-low incidences of population and arrest density.  
Those high-high and low-low areas are those where the population and arrest densities are similar, and follow that weak positive relationship linking the densities.  
The low-high and high-low areas are those which show that some other factors must influence the arrest rates, because that linking relationship is not followed.  

# Emergency Food Supply Gap - 2024 data mapped on 2020 Neighbourhood Tabulation Areas  

The Emergency Food Supply Gap dataset includes estimates for each neighbourhood of the gap between required and supplied emergency food, the percentage of food insecurity, the rate of unemployment, and the presence of vulnerable populations, those being under 18, 65 or older, foreign born non-citizens, or veterans.  

We are looking at this dataset in relation to arrest rates to see if there is a correlation between arrests and typically stated exacerbators of crime, like unemployment and food insecurity.

## 2024 arrest rates on 2020 Neighbourhood Tabulation Areas
<img width="2928" height="1926" alt="Image" src="https://github.com/Tmalthus/nycdata/blob/main/nta2020_arrest_counts.png" />  

We see high rates of arrests in midtown Manhattan, Harlem, South Bronx, North and East Queens, South and East Brooklyn, and North Eastern Staten Island.

## 2024 food insecurity  
<img width="2928" height="1926" alt="Image" src="https://github.com/Tmalthus/nycdata/blob/main/nta2020_foodinsecurity_yellow_high.png" />  

The highest rates of food insecurity are indicated in yellow. These areas include The Bronx, Harlem, and East Brooklyn, which also have high arrest rates. However there are areas with high arrest rates and without high food insecurity, such as midtown Manhattan, and North and East Queens.  

## 2024 unemployment estimates  
<img width="2928" height="1926" alt="Image" src="https://github.com/Tmalthus/nycdata/blob/main/nta2020_unemployment_yellow_high.png" />  

The highest rates of unemployment are indicated in yellow. These areas include The Bronx, Harlem, East Brooklyn, and East Queens, which also have high arrest rates.  

Most of these areas are those same areas with high food insecurity.  

## 2024 vulnerable populations
<img width="2928" height="1926" alt="Image" src="https://github.com/Tmalthus/nycdata/blob/main/nta2020_vulnerable_pop_yellow_high.png" />  

## Pairs plot of arrest rates and food and vulnerability estimates  
<img width="2928" height="1926" alt="Image" src="https://github.com/Tmalthus/nycdata/blob/main/nta2020_arrests_food_insecurity_pairs.png" />  

