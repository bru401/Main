# Airbnb Rio X Security 

In this project I hope to accomplish a insightful analysis on the relationship between Airbnb pricing and the criminal rate in different Rio de Janeiro neighbourhoods.

## Data Source
This project is mainly based on two different datasets: 

### Inside Airbnb
[Inside Airbnb](https://insideairbnb.com/) provides data on the popular online marketplace for short-and-long term homestays. Naturally, as the touristic center of Brazil, the city of Rio de Janeiro is full of Airbnb lodgings, and that is what is reflected in the data with there being around 40k entries in the March 2025 listings.

### Instituto de Segurança Pública
This [institute of public security](https://www.ispdados.rj.gov.br/Notas.html) under the government of the state of Rio de Janeiro (which naturally encompasses the city) has released open data on the recorded crimes, sorted by the police districts.

## Process

The following project takes place in multiple steps:
Preliminary Data Analysis of the Airbnb dataset
1) BnBRio_Neighbourhoods
2) BnBRio_DataAnalysis
Preliminary Data Analysis of the Security dataset
3)

## BnBRio_Neighbourhoods
In antecipation to the matching of the two different datasets through the city's neighbourhoods, we will first create a .csv file with the following columns:
* Neighbourhood
* RISP
* AISP
* CISP
* Neighbourhood Group (known as 'zones' in Rio)
RISP, AISP and CISP refer to the police districts by which the public security dataset is ordered by.
 
The dificulty lies in the fact that the Aribnb dataset is organized by neighbourhood whilst the public security is organized by 'territory units' ('Unidade Territorial') which include one or more neighbourhoods.
Fortunately, the following table will allow us to translate those territorial units into neighbourhoods and match the two datasets.
