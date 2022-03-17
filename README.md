# Will Vaccination Help Reduce Spread of Covid-19 in El Paso County?

## Research Motivation

The spread of SARS-CoV-2, the causative agent of COVID-19, has resulted in an unprecedented global public health and economic crisis. The outbreak was declared a pandemic by the World Health Organization on 11 March 2020, and development of COVID-19 vaccines has been a major undertaking in fighting the disease. It is estimated that a novel COVID-19 vaccine will need to be accepted by at least 55% of the population to provide herd immunity, with estimates reaching as high as 85% depending on country and infection rate. Reaching these required vaccination levels should not be assumed given well-documented evidence of vaccination hesitancy across the world, which is often fueled by online and offline misinformation surrounding the importance, safety, or effectiveness of vaccines. There has been widely circulating false information about the pandemic on social media platforms, such as 5G mobile networks are linked with the virus, vaccine trial participants have died after taking a COVID-19 vaccine, and the pandemic is a conspiracy or a bioweapon. Such information can build on pre-existing fears, seeding doubt and cynicism over new vaccines, and threatens to limit public uptake of COVID-19 vaccines. 

Therefore, in this research, we would like to investigate the impact of mask mandate and Covid 19 vaccine administration on the spread of the disease in El Paso County in Colorado State. We also strive towards increasing the awareness of the importance of Covid-19 vaccination and help change the perspective of unvaccinated people towards the need for vaccination. 

## Data

The common analysis research question will require several different datasets. We will need:  

1. The [RAW_us_confirmed_cases.csv](https://www.kaggle.com/antgoldbloom/covid19-data-from-john-hopkins-university?select=CONVENIENT_us_confirmed_cases.csv) file from the Kaggle repository of John Hopkins University COVID-19 data.  


Rows: 3342   
Data columns (total 658 columns):   

Columns | Non-Null Count | Dtype 
--- | ------ | ------ 
Province_State | 3342 non-null | object 
Admin2 | 3342 non-null | object 
UID | 3342 non-null | int64 
iso2 | 3342 non-null | object    
iso3 | 3342 non-null | object 
code3 | 3342 non-null | int64   
FIPS | 3342 non-null | float64 
Country_Region | 3342 non-null | object 
Lat | 3342 non-null | float64   
Long_ | 3342 non-null | float64 
Combined_Key | 3342 non-null | object 
1/22/20 | 3342 non-null | int64
...10/29/2021 | 3342 non-null | int64

2. The [RAW_us_deaths.csv](https://www.kaggle.com/antgoldbloom/covid19-data-from-john-hopkins-university?select=CONVENIENT_us_confirmed_cases.csv) file from the Kaggle repository of John Hopkins University COVID-19 data.    

Rows: 3342   
Data columns (total 687 columns):   

Columns | Non-Null Count | Dtype 
--- | ------ | ------ 
Province_State | 3342 non-null | object 
Admin2 | 3342 non-null | object 
UID | 3342 non-null | int64 
iso2 | 3342 non-null | object    
iso3 | 3342 non-null | object 
code3 | 3342 non-null | int64   
FIPS | 3342 non-null | float64 
Country_Region | 3342 non-null | object 
Lat | 3342 non-null | float64   
Long_ | 3342 non-null | float64 
Combined_Key | 3342 non-null | object 
Population | 3342 non-null | int64  
1/22/20 | 3342 non-null | int64
...11/26/2021 | 3342 non-null | int64

3. The CDC dataset of [masking mandates by county](https://data.cdc.gov/Policy-Surveillance/U-S-State-and-Territorial-Public-Mask-Mandates-Fro/62d6-pm5i).  

Rows: 3142   
Data columns (total 6 columns):   

Columns | Non-Null Count | Dtype 
--- | ------ | ------ 
COUNTYFP | 3142 non-null | int64 
NEVER | 3142 non-null | float64 
RARELY | 3142 non-null | float64    
SOMETIMES | 3142 non-null | float64 
FREQUENTLY | 3142 non-null | float64   
ALWAYS | 3142 non-null | float64 
 
4. The New York Times [mask compliance survey](https://github.com/nytimes/covid-19-data/tree/master/mask-use) data. 
  
Rows: 1593869   
Data columns (total 10 columns):   

Columns | Non-Null Count | Dtype 
--- | ------ | ------ 
State_Tribe_Territory | 1593869 non-null | object 
County_Name | 1593869 non-null | object 
FIPS_State | 1593869 non-null | int64    
FIPS_County | 1593869 non-null | int64 
date | 1593869 non-null | object   
order_code | 1593869 non-null | int64 
Face_Masks_Required_in_Public | 987555 non-null | object 
Source_of_Action | 987555 non-null | object   
URL | 987555 non-null | object 
Citation | 987555 non-null | object  

5. [COVID-19 Vaccinations in the United States,County](https://data.cdc.gov/Vaccinations/COVID-19-Vaccinations-in-the-United-States-County/8xkx-amqh) data.   

Rows: 1138678   
Data columns (total 32 columns):   

Columns | Non-Null Count | Dtype 
--- | ------ | ------ 
Date | 1138678 non-null | object 
FIPS | 1138678 non-null | object 
MMWR_week | 1138678 non-null | int64    
Recip_State | 1138678 non-null | object 
Recip_County | 1138678 non-null | object   
Series_Complete_Pop_Pct | 1138678 non-null | float64 
Series_Complete_Yes | 1138678 non-null | int64   
Series_Complete_12Plus | 1123066 non-null | float64 
Series_Complete_12PlusPop_Pct | 1123066 non-null | float64 
Series_Complete_18Plus | 1138678 non-null | int64 
Series_Complete_18PlusPop_Pct | 1138678 non-null | float64    
Series_Complete_65Plus | 1138678 non-null | int64 
Series_Complete_65PlusPop_Pct | 1138678 non-null | float64   
Completeness_pct | 1138678 non-null | float64 
Administered_Dose1_Recip | 1103077 non-null | float64 
Administered_Dose1_Pop_Pct | 1138678 non-null | float64
Administered_Dose1_Recip_12Plus | 1060802 non-null | float64 
Administered_Dose1_Recip_12PlusPop_Pct | 1123066 non-null | float64 
Administered_Dose1_Recip_18Plus | 1076215 non-null | float64    
Administered_Dose1_Recip_18PlusPop_Pct | 1138678 non-null | float64 
Administered_Dose1_Recip_65Plus | 1076215 non-null | float64   
Administered_Dose1_Recip_65PlusPop_Pct | 1138678 non-null | float64 
SVI_CTGY | 1116993 non-null | object   
Series_Complete_Pop_Pct_SVI | 913868 non-null | float64
Series_Complete_12PlusPop_Pct_SVI | 900567 non-null | float64 
Series_Complete_18PlusPop_Pct_SVI | 913868 non-null | float64 
Series_Complete_65PlusPop_Pct_SVI | 913868 non-null | float64    
Series_Complete_Pop_Pct_UR_Equity | 913001 non-null | float64 
Series_Complete_12PlusPop_Pct_UR_Equity | 899833 non-null | float64   
Series_Complete_18PlusPop_Pct_UR_Equity | 913212 non-null | float64 
Series_Complete_65PlusPop_Pct_UR_Equity | 912495 non-null | float64  


## Methods
In this research, we would like to see if vaccination will help reduce the spread of the disease by using the data from El Paso County in Colorado States. The questions we were trying to answer are:   
1.	How did mask mandate policy help to reduce the spread of the disease?   
2.	How did Covid-19 vaccine administration help reduce the spread of the disease?  
3.	Did vaccination help with the decrease in daily Covid death?  

In this analysis, we will first use visualization to see if there is any potential association between mask mandate policy and the daily confirmed cases. Then we will use hypothesis testing with ordinary least-squares method to investigate the impact of Covid-19 vaccination administration on the spread of the disease.   

The null hypothesis for the second and third research are as follows:   
1) There is no association between the number of total vaccinated people and total confirmed cases in El Paso County.  
2) There is no association between the number of total vaccinated people and the number of daily newly confirmed cases in El Paso County.  
3) There is no association between the number of total vaccinated people and the increase in total death (caused by Covid19) in El Paso County.  


## Limitations
There are four main limitations for this research.    
- First, the model assumptions are not well met due to the skewed data so the results of the model can be used to understand basic associations but should not be taken too literally or used for prediction. Other model should be applied before drawing any conclusions.    
- Second, the associations found in this analysis may not translate to other counties, states, and countries.    
- Third, this analysis does not completely capture the associations the completely vaccinated and confirmed cases and total covid death.    
- Finally, other influencing factors such as recovery data and more vaccination data could be considered for further analysis. The lack of vaccination data from Dec.2020 to May 24th, 2021 may not very well explain the impact of vaccine administration on reducing the spread of Covid-19 regarding other factors such as stay-at-home order, mask mandate policy, etc.   
