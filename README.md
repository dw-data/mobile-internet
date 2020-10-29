# Prices for mobile internet in African countries

You can read the story [here]()

Idea, research and writing: [David Ehl](https://twitter.com/david_ehl)

Data analysis and visualization: [Gianna-Carina Grün](https://twitter.com/giannagruen)


## Data sources

### Mobile data prices

The **source** for mobile internet prices is the British telecom provider Cable UK, given that they provided the most recent data (beginning of 2020). The data was [downloaded from their website](https://www.cable.co.uk/mobiles/worldwide-data-pricing/). 

There, they also included more detail on the scope of their research project: *Data from 5,554 mobile data plans in 228 countries were gathered and analysed by Cable.co.uk between 3 February and 25 February 2020. The average cost of one gigabyte (1GB) was then calculated and compared to form a worldwide mobile data pricing league table.*

**Key variable description** According to their [methodological description of the data](https://s3-eu-west-1.amazonaws.com/assets.cable.co.uk/mobile-data-cost/global-broadband-pricing-study-2020-methodology.pdf) the core variables in the dataset are defined as follows:

* "Plans measured": *Researchers first established the mobile data providers in each country before selecting one SIM plan from each data amount they offer. A country with eight providers, for example, each offering three different SIM data sizes, will have 24 plans recorded (...) Packages were recorded up to a maximum of 60 per country – records beyond this number have negligible impact on the average (...) This number will always be between 3 and 60.*

* "Average price":  *Averages are calculated as the MEDIAN of all recorded package prices/data limits. (...)  The average monthly cost of 1GB of data for each country as a whole is calculated as the MEDIAN of every plan recorded*

* "Sample date" / Price data : *The 'Sample date' column is very important as it represents the day the data was collected for that particular country. It is a snapshot. Prices change all the time and therefore may be different by the time you go about viewing and/or utilising our data* 

**Gaps in the data**: According to their description, the following African countries missing from the dataset:

| Name | Continental region | Missing data reason |
|-----------|---------------|---------------------|
|Eritrea | NORTHERN AFRICA | NO PROVIDERS |
|Congo (Democratic Republic of) | SUB-SAHARAN AFRICA | PRICES ONLY IN 'UNITS' |
|Zimbabwe | SUB-SAHARAN AFRICA | UNRELIABLE EXCHANGE RATES |
|South Sudan | SUB-SAHARAN AFRICA | NO PROVIDERS |
|North Korea | ASIA | NO PROVIDERS |
|St. Pierre and Miquelon | CARIBBEAN | NO PROVIDERS |
|Christmas Island | CARIBBEAN | NO PROVIDERS |
|Venezuela | SOUTH AMERICA | NO PROVIDERS |
|Wallis and Futuna | OCEANIA | NO PROVIDERS |
|Marshall Islands | OCEANIA | NO PROVIDERS |
|Cook Islands | OCEANIA | NO PROVIDERS |
|Tuvalu | OCEANIA | NO PROVIDERS |


**Data caveats**: It's important to consider the high volatility of pricing data. A research analyst of CableUK comments: *"When it comes to the cost of 1GB pricing can change dramatically over time since changes to the data sizes available can happen overnight."* Thus, the data should be seen as snapshots of a certain point in time.


**Other data sources**: We also considered the mobile pricing data by the [ITU (International Telecommunication Union)](https://www.itu.int/en/mediacentre/Documents/Documents/ITU-Measuring_Digital_Development_ICT_Price_Trends_2019.pdf) as well as by the [A4AI (Alliance for Affordable Internet)](https://a4ai.org/extra/mobile_broadband_pricing_gnicm-2019Q2). The main reason to decide against both sources was that the CableUK data is more recent (Q1 2020 vs Q2 2019). Additionally, the ITU data is more granular: offering different ["baskets"](https://www.itu.int/en/ITU-D/Statistics/Documents/ICT_Prices/ICT%20Price%20Basket%20rules_E.pdf) with different data volumes which was not necessary to answer our initial research question.


### Monthly national income

The data on national income was taken from **The World Bank**, who publishes the [_Gross national income per capita_](https://data.worldbank.org/indicator/NY.GNP.PCAP.CD) by country and by year. We used the GNI per capita, according to the [Atlas method (current US$)](https://databank.worldbank.org/reports.aspx?source=2&type=metadata&series=NY.GNP.PCAP.CD)

Because the data for mobile prices are monthly, we divided the World Bank data by 12 to arrive at the _monthly GNI per capity (in current US$)_ we used for our analysis.

The GNI is provided for different years for different countries; we used the latest available data for each country. 


## Definitions

The Alliance for Affordable Internet [defines](https://a4ai.org/affordable-internet-is-1-for-2): _"affordable internet is where 1GB of mobile broadband data is priced at 2% or less of average monthly income."_ This recommendation has also been [adopted](https://a4ai.org/un-broadband-commission-adopts-a4ai-1-for-2-affordability-target/) by the UN Broadband Commission for sustainable development as their new target.


## Methological decisions

We **excluded** Somalia from our analysis, because the latest available GNI data was from 1990, which we considered too outdated. We furthermore excluded Oceania, as the GNI data here was very gappy and would not have allowed for a solid regional average. Furthermore, for the analysis on African countries, we excluded the Comoros Islands, Sao Tome and Principe and Seychelles from our analysis and focused on countries with more than 850,000 inhabitants.

We **chose** to use the data for the median price instead of the cheapest price for 1GB of mobile internet per country, since this is more likely to reflect the given situation for end users (since it is unlikely the cheapest price per country is available to every person within that country).

We **refactored** the pricing data in order to reflect the affordability target (see definition). Instead of showing the percentage share each population on average spends on 1GB of mobile internet, we calculated off of the monthly national income what the two percent affordability benchmark would equal in US dollar.

We **relabelled** the CableUK data labelled as 2019 by the data provider as 2018 data, since only 2 samples were collected in 2019, whereas the other 228 samples were collected in Q4 2018.


## Results