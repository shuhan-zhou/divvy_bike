# divvy_bike

Group Members: 
Umer Naeem; 
Shuhan Zhou;
Isidoro Garcia 

Motivation:

DIVVY bike has increased steadily since 2013 where it was released. Of the key factors for its demand is the location. Whenever users want to start a trip, they a station close by for DIVVY to be a preferred transportation option. As a result, knowing what Users’ drive socio-economic characteristics drive DIVVY demand and where these users live can give light of where is optimal for stations to be. Using Zipcode socio-economic data from the Census Bureau and chicago local DIVVY trip data. We will track which socio-economic factor are most important to DIVVY demand. 

Question: whether DIVVY trip usage patterns vary by age, income and neighborhood in Chicago and hopefully come up with an estimate which factor out of the three contribute to the usage difference the most? 

Data:
DIVVY trips: https://data.cityofchicago.org/Transportation/Divvy-Trips-Dashboard/u94x-unre
Demographic data by zipcode: Census Bureau: https://www.census.gov/geo/maps-data/data/tiger-data.html

Analysis:
Estimate shifts on demands for DIVVY bikes based on age, gender, income by station. 

Data specifics that need to be taken into account:
DIVVY separates the trip starting location with the trip ending location. To address this, we will focus our analysis on start points, since the income data is based on where does the individuals live. Assuming the majority of the trips start near their houses and end wherever their destination is. 

Household socio-economic data is at Zipcode level, no block level, so we don’t have an exact geographical level match on the data. To address this, we will create buffers around divvy stations and take mean income level for household reside within that buffer. 

Finally, DIVVY data has both suscribers and costumers. Since costumers are usually eventual users, they probably don’t start their trip near their home. On the other hand, suscribers are regular users that use DIVVY bike for commuting to work or similars. Consequently, we will focus our analysis on suscribers, since this type of user fits better our assumptions. Moreover, looking at the DB of DIVVY bikes, most of the users are suscribers, should this shouldn’t entail a power issue. 



