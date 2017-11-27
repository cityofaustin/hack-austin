### 500 Cities Census Tract level

This is the complete dataset for the 500 Cities project. This dataset includes 2013, 2014 model-based small area estimates for 27 measures of chronic disease related to unhealthy behaviors (5), health outcomes (13), and use of preventive services (9). Data were provided by the Centers for Disease Control and Prevention (CDC), Division of Population Health, Epidemiology and Surveillance Branch. The project was funded by the Robert Wood Johnson Foundation (RWJF) in conjunction with the CDC Foundation. It represents a first-of-its kind effort to release information on a large scale for cities and for small areas within those cities. It includes estimates for the 500 largest US cities and approximately 28,000 census tracts within these cities. These estimates can be used to identify emerging health problems and to inform development and implementation of effective, targeted public health prevention activities. Because the small area model cannot detect effects due to local interventions, users are cautioned against using these estimates for program or policy evaluations. Data sources used to generate these measures include Behavioral Risk Factor Surveillance System (BRFSS) data (2013, 2014), Census Bureau 2010 census population data, and American Community Survey (ACS) 2009-2013, 2010-2014 estimates. More information about the methodology can be found at www.cdc.gov/500cities.

Column Name | Description
---|---------
`Year` | Year
`StateAbbr` | State abbreviation
`StateDesc` | State name
`CityName` | City name
`GeographicLevel` | Identifies either US, City or Census Tract
`DataSource` | Data source
`Category` | Topic
`UniqueID` | At city-level, it is the FIPS code of CityFIPS. For tract-level data, it is a combined ID of CityFIPS and TractFIPS for tracts within the respective city with the exception of Honolulu, which only uses TractFIPS
`Measure` | Measure full name
`Data_Value_Unit` | The data value unit, such as "%" for percentage
`DataValueTypeID` | Identifier for the data value type
`Data_Value_Type` | The data type, such as age-adjusted prevalence or crude prevalence
`Data_Value` | Data Value, such as 14.7
`Low_Confidence_Limit` | Low confidence limit
`High_Confidence_Limit` | High confidence limit
`Data_Value_Footnote_Symbol` | Footnote symbol
`Data_Value_Footnote` | Footnote text
`PopulationCount` | Population count from census 2010
`GeoLocation` | Latitude, longitude of city or census tract centroid
`CategoryID` | Identifier for Topic/Category
`MeasureId` | Measure identifier
`TractFIPS` | FIPS code
`Short_Question_Text` | Measure short name


Source: [Centers for Disease Control and Prevention](https://chronicdata.cdc.gov/).
