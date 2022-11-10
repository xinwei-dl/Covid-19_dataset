# Covid-19_dataset

* This dataset is used to predict county-level distribution of COVID-19 cases and deaths in the US, and to test the existence of bias whthin.  
* All datas are collected from public datasets, such as Google and government websites.   
* We did some preliminary work on the datasets to make them easier to be combined (each county is add with the countyFIP in each file) and feed into the models.  
* The spatial resolution of this dataset is at the county level, for time resolution, it is as fined as possible.  
  
  
==============================description of each dataset:)  
**1. cases deaths population**  
Collected from USAFACTS https://usafacts.org/visualizations/coronavirus-covid-19-spread-map  
Spatial resolution: county level, Temporal resolution: daily level, covers 3193 counties in 50 states and DC from Jan 22, 2020 to Nov 3, 2022.  
  
**2. population sex age race**  
Collected from The Census Bureau, modified according to the table " American Community Survey SO1O1 AGE AND SEX 2020: ACS 5-Year Estimates Subject Tables" https://data.census.gov/cedsci/table.  
Spatial resolution: county level, Temporal resolution: annual level, covers 3143 counties in 50 states and DC in 2020.  
This dataset contains the following factures:  
*Total population*  
*Male*  
*Female*  
*Median Age (years)*  
*18 years and over*  
*65 years and over*  
*Race alone or in combination with one or more other races (White/ Black or African American/ American Indian and Alaska Native/ Asian/ Native Hawaiian and Other Pacific Islander/ Some other race)*  
*Hispanic or Latino*  
This dataset is devided into two parts, one contains estimated values, the other contains the percentage of each segment in the total population.  
  
**3. occupation**  
Collected from The Census Bureau, modified according to the table " American Community Survey S24O1 OCCUPATION BY SEX FOR THE CIVILIAN EMPLOYED POPULATION 16 YEARS AND OVER 2020: ACS 5-Year Estimates Subject Tables" https://data.census.gov/cedsci/table.  
Spatial resolution: county level, Temporal resolution: annual level, covers 3143 counties in 50 states and DC in 2020.  
This dataset contains the following factures:  
*Healthcare practitioners and technical occupations*  
*Service occupations*  
*Sales and office occupations*  
*Natural resources, construction, and maintenance occupations*  
*Production, transportation, and material moving occupations*  
  
**4. health**  
Collected from  Centers for Disease Control and Prevention https://www.cdc.gov/chronicdisease/  
Spatial resolution: county level, Temporal resolution: annual level, covers 3142 counties in 50 states and DC.  
1) Current Smoker Status Among Adults Ages 18+, 2018  
2) Diagnosed Diabetes, Age-Adjusted Percentage, 20+, 2017  
3) Total Cardiovascular Disease Hospitalization Rate per 1,000 Medicare Beneficiaries, 2017-2019  
Unfortunately, the data was not collected very recently, mostly a few years ago.  

**5. Mobility_google**  
The dataset contains two mobility datas, this is the forst one, which is Google Community Mobility Report, the discription of the dataset can be viewed in the offical website.
It is collected from https://www.google.com/covid19/mobility/  
Spatial resolution: county level, Temporal resolution: daily level, covers about 1000 to 3000 counties in 50 states and DC from Feb 15, 2020 to Oct 15, 2022.  
We have modified the raw dataset to separate each variable for each year into a csv file.  
And we also changed the dimensionality of the data so that the column is data and the row is county.  
  
**6. geographic**  
This dataset contains the geographic location and adjacency relation between each county.  
The raw data is from GMAD https://gadm.org/download_country.html  
It is processed with ArcGIS, using which to extracted the latitude and longitude of each county, and to calculated the adjacency relation between each other.
