# NCDS Internship Tableau Workshop
Instructor: Peace Ossom-Williamson

Access data files at: <link in here>

Let’s explore the price of gasoline in the United States and vehicle travel behavior. Our data table comes from five data sets. All U.S. data are provided by Month from January 1993 to June 2022.

## About the Data Sources


### GAS PRICE DATA

Three data sets are recording the monthly price per gallon of gasoline in the United States, for the period of April 1993 to May 2022. Drawing on these data sets, we will be looking at fuel price information collected by the U.S. Bureau of Labor Statistics (2022), the U.S. Energy Information Administration (2022, June 13), and the Consumer Price Index (2022) by the U.S. Bureau of Labor Statistics.

#### Sources

1. gp_bls-unleaded: U.S. Bureau of Labor Statistics, Average Price: Gasoline, Unleaded Regular (Cost per Gallon/3.785 Liters) in U.S. City Average [APU000074714], retrieved from FRED, Federal Reserve Bank of St. Louis; <https://fred.stlouisfed.org/series/APU000074714>, June 19, 2022.
> The U.S. Bureau of Labor Statistics collects information about gasoline prices monthly from seventy-five urban areas of the United States monthly, through mail questionnaires. Variable definition: Average U.S. cost of unleaded regular gasoline per gallon by month.

2. gp_eia: U.S. Energy Information Administration. (2022, June 13). U.S. All Grades All Formulations Retail Gasoline Prices. U.S. gasoline and diesel retail prices [Data Set]. <https://www.eia.gov/dnav/pet/pet_pri_gnd_dcus_nus_a.htm>
> The information in this dataset is compiled by the U.S. Energy Information Administration, and collected at 8:00 a.m. Monday mornings, on a weekly basis at stations across the country. According to the Methodology for EIA Weekly Retail Gasoline Price Estimates, information on regular, mid-grade, and high-grade gasoline are collected, to provide a more balanced comparison of consumer prices available. These prices are then compiled to provide averages at the city, county, state, regional, and national levels. Variable definition: Weekly retail gasoline and diesel prices
(dollars per gallon).

3. gp_bls-all: U.S. Bureau of Labor Statistics. (2022). Top picks (most requested statistics) - Gasoline, all types, per gallon/3.785 liters in U.S. city average, average price, not seasonally adjusted & Gasoline, unleaded regular, per gallon/3.785 liters in U.S. city average, average price, not seasonally adjusted. U.S. Bureau of Labor Statistics - Consumer Price Index [Data set]. <https://data.bls.gov/cgi-bin/surveymost?ap>
> Similarly, to the unleaded information compiled for the U.S. Bureau of Labor Statistics, the 
Consumer Price Index information represents a national market, and does not limit their sampling to a specific geographic area. The index does differ in that they attempt to regularly rotate the locations where they sample product prices, and do not adjust data for seasonal availability, which more accurately reflects the market (CPI: Average price data). Variable definition: Average U.S. cost of all types gasoline per gallon by month.

### MILES TRAVELED DATA

The data for miles traveled will show how many total miles vehicles traveled that month.

#### Source

4. Milestraveled_inM: U.S. Federal Highway Administration, Vehicle Miles Traveled [TRFVOLUSM227NFWA], retrieved from FRED, Federal Reserve Bank of St. Louis; <https://fred.stlouisfed.org/series/TRFVOLUSM227NFWA>, June 23, 2022.
> Vehicle Miles Traveled and the 12-Month Moving Vehicle Miles Traveled series are created by appending the recent monthly figures from the FHWA’s Traffic Volume Trends to their Historic Monthly Vehicle Miles Traveled (VMT) data file. Variable definition: Total vehicle miles traveled in the U.S. by month, given in millions.


### STATE AND MSA DATA

Vehicle-related data for states and metropolitan statistical areas is provided from one data source. 

#### Source

5. U.S. Department of Transportation. (2015, October 27). Transportation and Health Tool. <https://www7.transportation.gov/transportation-health-tool>

The variables include
| Variable Name             | Variable Definition                                                                |
|---------------------------|------------------------------------------------------------------------------------|
|     Location              |     Name of the state or MSA                                                       |
|     Loc_Type              |     Type of location. 2 possible values: State, Metropolitan   Statistical Area    |
|     DUI_rate              |     DUI/DWI Fatalities per 10,000 Residents: Raw Value                             |
|     DUI_score             |     DUI/DWI Fatalities per 10,000 Residents: Score*                                |
|     personmiles           |     Distance a Person Travels in a Year by Private Vehicle: Raw Value              |
|     vehiclemiles          |     Total annual miles of vehicle travel per Capita: Raw Value                     |
|     vehiclemiles_score    |     Vehicle Miles Traveled per Capita: Score*                                      |

\* *To make results easier to interpret, the website provides scores for states, metropolitan statistical areas, and urbanized areas on a scale of 0 to 100, where higher values are better. The score for a given state or area represents its percentile value. This is the percent of states or regions that score below it. Read more about how scores are calculated at <https://www7.transportation.gov/mission/health/tool-scoring-methodology>*

### SHAPEFILE

The MSA shapefile comes from one data source. It must be downloaded and used as a ZIP file.

6. U.S. Census Bureau. (2021, October 12). TIGER/Line Shapefile, 2019, nation, U.S., Current Metropolitan Statistical Area/Micropolitan Statistical Area (CBSA) National [Data set]. <https://catalog.data.gov/dataset/tiger-line-shapefile-2019-nation-u-s-current-metropolitan-statistical-area-micropolitan-statist>

## Tableau Steps

### Connecting to Data and Joining Tables
1. Upload the Excel file in Tableau using the left menu. Change to "Extract" since we will have more than one data source.

<img src="img/img-01.jpg" width=30%>

2. Change data types as needed. You can create calculated fields here or later while in the sheets.

<img src="img/img-02.jpg" width=50%>

3. To connect to the shapefile, click "Add." Then select "Spatial File." Select the zip file.

<img src="img/img-03.jpg" width=50%>

4. To join these two, double-click the `data_table` in the center of the page. (Or, right-click and select "Open.") Complete a left join using "Location" for the data_table and "Name" for the shape file. As a secondary effort to ensure correct matching, you can also indicate that the "Loc Type" variable should equal "Metropolitan Statistical Area" in a custom join calculation.

<img src="img/img-04.jpg" width=50%><img src="img/img-05.jpg" width=50%>
*Note: There should still be 785 rows.*

### Creating a Bar Chart

5. Click on "Sheet 1" at the bottom to create your first visualization.

<img src="img/img-06.jpg" width=30%>
*Note: Tableau will prompt you to save the data extract. Press the "Save" button.*

6. 


How to add a link: [Duck Duck Go](https://duckduckgo.com)
