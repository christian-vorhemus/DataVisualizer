#INQStats API Data Visualization Example

This example shows how to use the INQStats API provided at [inqstatsapi.inqubu.com](http://inqstatsapi.inqubu.com). To get started, request an API key [here](http://blog.inqubu.com/inqstats-open-api-published-to-get-demographic-data). 

The API is accessible via REST interface. The following parameters can be passed in the request:
<p></p>
<table border="1" style="width:600px;">
<tbody><tr>
<td style="width:100px"><b>Key</b></td>
<td><b>Description</b></td>
<td><b>Cardinality</b></td></tr>
<tr>
<td>api_key</td>
<td>This is a mandatory value. It must be provided with every request. Please fill in the form above to get your personal API key.</td>
<td>1</td>
</tr>
<tr>
<td>data</td>
<td>A list of data keys that should be returned, separated by commas without spaces (please see list below to get an overview about all available data keys).</td>
<td>1...*</td>
</tr>
<tr>
<td>countries</td>
<td>A list of countries for which data should be returned. Please use the ISO 3166-1 alpha-2 format for countries separated by commas without spaces (e.g. us = United States, de = Germany, etc.)</td>
<td>1...*</td>
</tr>
<tr>
<td>years</td>
<td>Optional. It can be used to get data from a specific year. If this parameter is not set, the five most up to date values are returned. Use a comma separated list to get data from several years (e.g. years=2011,2012,2013), you can also set a range (e.g. years=2011:2013 which will return all data between 2011 and 2013 if available)</td>
<td>0...*</td>
</tr>
<tr>
<td>lang</td>
<td>Optional. States, in which language values are returned. Available options are: en (English; default), de (German), es (Spanish), pt (Portuguese), fr (French), it (Italian), ru (Russian), zh (Chinese).</td>
<td>0...1</td>
</tr>
</table>
<p></p>
Subsequently, a list of all available data keys is given:
<p></p>
<table border="1" style="width:600px;">
<tbody><tr><td style="width:100px"><b>Key</b></td>
<td><b>Description</b></td><td><b>Source</b></td></tr>
<tr>
<td>bigmac_index</td>
<td>Returns the price for a Big Mac by McDonald's™ derived from www.bigmacindex.org (unit: USD).</td>
<td>www.bigmacindex.org</td>
</tr>
<tr>
<td>birth_rate</td>
<td>The average number of birth per year per 1,000 population.</td>
<td>Worldbank</td>
</tr>
<tr>
<td>co2_emissions</td>
<td>Returns the CO2 emissions in metric tons per person per year.</td>
<td>Global Carbon Atlas</td>
</tr>
<tr>
<td>corruption_index</td>
<td>Returns the Corruption Perceptions Index (CPI) published by www.transparency.org (scale: 0-100; 0 = high corruption. 100 = low corruption)</td>
<td>www.transparency.org</td>
</tr>
<tr>
<td>density</td>
<td>Returns the population density of a country (per km²).</td>
<td>-</td>
</tr>
<tr>
<td>death_rate</td>
<td>The average number of death per year per 1,000 population.</td>
<td>Worldbank</td>
</tr>
<tr>
<td>debts</td>
<td>The total amount of government borrowings (unit: USD).</td>
<td>Worldbank</td>
</tr>
<tr>
<td>debts_capita</td>
<td>The amount of government borrowings per person (unit: USD).</td>
<td>Worldbank</td>
</tr>
<tr>
<td>debts_percent</td>
<td>The percentage of government borrowings in relation to the GDP.</td>
<td>Worldbank</td>
</tr>
<tr>
<td>diabetes_prevalence</td>
<td>The percentage of people ages 20-79 who have type 1 or type 2 diabetes.</td>
<td>Worldbank</td>
</tr>
<tr>
<td>education_expenditure</td>
<td>Returns the public expenditure on education (in % of the GDP for a country).</td>
<td>Worldbank</td>
</tr>
<tr>
<td>electric_energy_consumption</td>
<td>Returns the amount of electric energy consumed (in kWh/capita)</td>
<td>Worldbank</td>
</tr>
<tr>
<td>fifa</td>
<td>Returns the ranking of a country in the FIFA™ football ranking board.</td>
<td>www.fifa.com</td>
</tr>
<tr>
<td>first_marriage_men</td>
<td>Returns the age of first marriage for men.</td>
<td>Worldbank</td>
</tr>
<tr>
<td>first_marriage_women</td>
<td>Returns the age of first marriage for women.</td>
<td>Worldbank</td>
</tr>
<tr>
<td>fixed_telephone_subscriptions</td>
<td>Returns the number of landline phone subscriptions (per 100 population)</td>
<td>Worldbank</td>
</tr>
<tr>
<td>forest_area</td>
<td>Returns the total amount of forest area in a country (in km²)</td>
<td>Worldbank</td>
</tr>
<tr>
<td>forest_area_percent</td>
<td>Returns the percentage of the land area covered by a forest for a country.</td>
<td>Worldbank</td>
</tr>
<tr>
<td>gdp_total</td>
<td>Returns the total Gross Domestic Product (GDP) for a country (unit: USD).</td>
<td>Worldbank</td>
</tr>
<tr>
<td>gdp_capita</td>
<td>Returns the Gross Domestic Product per person for a country (unit: USD).</td>
<td>Worldbank</td>
</tr>
<tr>
<td>gini</td>
<td>Returns the Gini coefficient. The Gini coefficient states how uniformly assets are distributed in a country (scale: 0-100; 0 = equal distribution. 100 = unequal distribution)</td>
<td>Worldbank</td>
</tr>
<tr>
<td>happiness_index</td>
<td>Returns the values of the <a href="http://worldhappiness.report/" target="_blank">world happiness survey</a> of the UNSDSN. The higher the value, the happier the country.</td>
<td>UNSDSN</td>
</tr>
<tr>
<td>hdi</td>
<td>Returns the Human Development Index (HDI). It is published by the United Nations and combines several parameters (e.g. life expectancy or GDP). Scale: 0-1; 0 = low development. 1 = high development.</td>
<td>UN-Data</td>
</tr>
<tr>
<td>health_expenditure</td>
<td>Returns the public expenditure on health (in % of the GDP for a country).</td>
<td>Worldbank</td>
</tr>
<tr>
<td>hiv_prevalence</td>
<td>The percentage of people ages 15-49 who are infected with HIV</td>
<td>Worldbank</td>
</tr>
<tr>
<td>inflation</td>
<td>Returns the annual change of consumer prices (unit: %).</td>
<td>Worldbank</td>
</tr>
<tr>
<td>internetuser</td>
<td>Returns the total number of people that are actively using the internet.</td>
<td>Worldbank</td>
</tr>
<tr>
<td>internetusers_percent</td>
<td>Returns the percentage of people, that are actively using the internet for a country.</td>
<td>Worldbank</td>
</tr>
<tr>
<td>jobless_rate</td>
<td>The number of unemployed people in relation to the labor force for a country.</td>
<td>Worldbank</td>
</tr>
<tr>
<td>life_expectancy</td>
<td>The average number of years a person will live (at birth).</td>
<td>UN-Data</td>
</tr>
<tr>
<td>literacy_rate</td>
<td>Returns the percentage of people, that have the ability to read and write by the age of 15.</td>
<td>Worldbank</td>
</tr>
<tr>
<td>medianwage</td>
<td>Returns the median monthly wage before taxes including public benefits (e.g child allowance); unit: USD.</td>
<td>Worldbank</td>
</tr>
<tr>
<td>median_age</td>
<td>The median age of the population.</td>
<td>UN-Data</td>
</tr>
<tr>
<td>migration</td>
<td>Returns the total number of people that emigrated or immigrated.</td>
<td>UN-Data</td>
</tr>
<tr>
<td>migration_rate</td>
<td>Returns the net migration rate (per 1,000 population).</td>
<td>UN-Data</td>
</tr>
<tr>
<td>military_expenditure</td>
<td>Returns the military budget (in % of the GDP for a country).</td>
<td>Worldbank</td>
</tr>
<tr>
<td>mobile_cellular_subscriptions</td>
<td>Returns the number of mobile phone subscriptions (per 100 population)</td>
<td>Worldbank</td>
</tr>
<tr>
<td>murder_rate</td>
<td>Returns the number of homicides (per 100,000 population).</td>
<td>UNODC</td>
</tr>
<tr>
<td>new_businesses_registered</td>
<td>Number of new limited liability corporations registered in the calendar year.</td>
<td>Worldbank</td>
</tr>
<tr>
<td>olympicsummergames_goldmedals</td>
<td>Returns the number of gold medals a country won at the Olympic Games.</td>
<td>IOC</td>
</tr>
<tr>
<td>olympicsummergames_silvermedals</td>
<td>Returns the number of silver medals a country won at the Olympic Games.</td>
<td>IOC</td>
</tr>
<tr>
<td>olympicsummergames_bronzemedals</td>
<td>Returns the number of bronze medals a country won at the Olympic Games.</td>
<td>IOC</td>
</tr>
<tr>
<td>population</td>
<td>Returns the population of a country.</td>
<td>UN-Data</td>
</tr>
<tr>
<td>population_0_14</td>
<td>Returns the percentage of people between the age 0 and 14.</td>
<td>Worldbank</td>
</tr>
<tr>
<td>population_15_64</td>
<td>Returns the percentage of of people between the age 15 and 64.</td>
<td>Worldbank</td>
</tr>
<tr>
<td>population_over_64</td>
<td>Returns the percentage of people who are older than 64 years.</td>
<td>Worldbank</td>
</tr>
<tr>
<td>pressfreedom_index</td>
<td>Returns an index derived from "Reporters without borders" that reflects how free the press of a country is. The lower the value, the better the freedom of press.</td>
<td>www.rsf.org</td>
</tr>
<tr>
<td>research_expenditure</td>
<td>Returns the public expenditures on scientific research (in % of the GDP for a country).</td>
<td>Worldbank</td>
</tr>
<tr>
<td>scientific_journal_articles</td>
<td>The number of scientific publications in medical or natural sciences.</td>
<td>Worldbank</td>
</tr>
<tr>
<td>size</td>
<td>Returns the area of a country (unit: km²).</td>
<td>UN-Data</td>
</tr>
<tr>
<td>tax_revenue</td>
<td>Compulsory transfers to the central government for public purposes (in % of the GDP for a country).</td>
<td>Worldbank</td>
</tr>
<tr>
<td>tax_revenue_total</td>
<td>Compulsory transfers to the central government for public purposes (in US-Dollar).</td>
<td>Worldbank</td>
</tr>
<tr>
<td>tourist_arrivals</td>
<td>The number of foreign citizens that stayed at least one night in the country. This includes hotel stays, transfers, conference visits, etc.</td>
<td>UN-Data</td>
</tr>
<tr>
<td>tourism_expenditure</td>
<td>The amount of expenditures dedicated for tourism (in % of the GDP for a country).</td>
<td>UN-Data</td>
</tr>
<tr>
<td>urban_population</td>
<td>Returns the percentage of people who live in a city.</td>
<td>Worldbank</td>
</tr>
</table>
<p></p>
If there is no value to display, either "null" or "N/A" in string format is returned.<br>
In the following, a sample request is given. This will return the population of the last five years of the United States and Great Britain (note, that you have to replace the api_key parameter with your own key):
<p></p>
<div style="height:auto;width:100%;background-color:#F5F5F5;font-family:'Courier New';font-size:11px;border:1px solid grey;padding:5px;text-align:left;">
GET http://inqstatsapi.inqubu.com?api_key=ADDYOURKEYHERE&data=population&countries=us,gb
</div>
