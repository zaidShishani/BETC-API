# Investigating APIs

I will be Investigating the APIs I used in city-explorer, I have used 3 different APIs in this project :

* LocationIQ
* Weatherbit
* TheMovieDB

## 1. API Description

* LocationIQ: provide lcoations ,map, latitude and longitude for developers.

* Weatherbit: provide the current weather from over 47,000 live weather stations and also give us previous weather history we can retrieve this data via city name, city ID ,weather station ID, zip code

* TheMovieDB: Is a community built API where they have filled it with a database of movie and TV shows from name, description,rating..etc.

## 2. API Usage

By submitting a city name each API will give us:

* LocationIQ: Will return a static map name of the city latitude and longitude.

* Weatherbit: Will return a description of the weather and date for the previous 16 days for the city name.

* TheMovieDB: Will return a picture of the poster of the movie along with the title,an overview,average votes, total votes, popularity, Released year based on if the movie contains the name of the city.

## 3. API Endpoints/Request URLs

* LocationIQ:

  * has two endpoint locations  on based in the US and on in Europe I used the US end point.

  * I used a request URL in city explorer: `https://us1.locationiq.com/v1/search.php?key=${process.env.REACT_APP_LOCATION_KEY}&q=${this.state.searchQuery}&format=json`.

* Weatherbit:

  * Has multiple Endpoints I to get forecast by the city name required parameter are city,county(optional).

  * I used a request URL in the back-end of city explorer: `https://api.weatherbit.io/v2.0/forecast/daily?key=${process.env.WEATHER_API_KEY}&city=${cityName}`.

* TheMovieDB:
    * It has only one Endpoint 

    * I used a request URL in the back-end of city explorer: `https://api.themoviedb.org/3/search/movie?api_key=${process.env.MOVIE_API_KEY}&query=${searchQuerey}`

## 4. Authentication Key

I'll be using Using Access Key Tokens. for all the APIs

* LocationIQ: Using Access Key Tokens.

* Weatherbit: Using Access Key Tokens.

* TheMovieDB: Using Access Key Tokens.

. Authentication Key

References:

* <https://www.themoviedb.org/about> - TMBD
* <https://locationiq.com/about> - LocationIQ
* <https://www.weatherbit.io/api> - Weatherbit
