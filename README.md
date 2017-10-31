# divvy_bike

Group Members: 
Umer Naeem; 
Shuhan Zhou;
Isidoro Garcia 

Motivation:

DIVVY bike's popularity in Chicago has increased steadily since 2013 when it was first released. Among the key factors influencing its demand is location choices of the bike stations. Intuitively, whenever users want to start a trip, they'd prefer a station closer by rather than one further away. Observations in different neighborhoods also suggest variations in the number of bike stations the company chooses to set up. Similar to the demand for other types of goods and services, we imagine users' socio-economic characteristics would impact DIVVY demand and then features of neighborhoods where potential users live can give light of where is optimal to set up new stations. Using Zipcode socio-economic data from the Census Bureau and chicago local DIVVY trip data, we will track which socio-economic factor are the most important in determining DIVVY demand. 

Question: 
Whether DIVVY trip usage patterns vary by age, income and neighborhood in Chicago and hopefully come up with an estimate which factor out of the three contribute to the usage difference the most? 

Data:
DIVVY trips: https://data.cityofchicago.org/Transportation/Divvy-Trips-Dashboard/u94x-unre
Demographic data by zipcode: Census Bureau: https://www.census.gov/geo/maps-data/data/tiger-data.html

Analysis:
Estimate shifts on demands for DIVVY bikes based on age, gender, income by station. 

Data specifics that need to be taken into account:

DIVVY separates the trip starting location with the trip ending location. To address this, we will focus our analysis on start points, since the income data is based on where does the individuals live. Assuming the majority of the trips start near their houses and end wherever their destination is. 

Household socio-economic data is at Zipcode level, no block level, so we don’t have an exact geographical level match on the data. To address this, we will create buffers around divvy stations and take mean income level for household reside within that buffer. 

Finally, DIVVY data classifies its users as "suscribers" and "customers" (which are one time users without registration). Therefore, information of customers is missing from the data and we will not include them as part of this analysis. On the other hand, suscribers are regular users that use DIVVY bike for commuting to work or similar purposes. Consequently, we will focus our analysis on suscribers, since this type of user fits better our assumptions. Moreover, looking at the DB of DIVVY bikes, most of the users are suscribers, should this shouldn’t entail a power issue. 



