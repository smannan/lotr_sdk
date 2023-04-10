### System requirements

Python 3.8.9


### Installation

pip install smannan-lotr-sdk

pip install requests


### Environment set up

This SDK will require an access key to use the Lord of the Rings Movie API.

Acquire an access key by signing up here: https://the-one-api.dev/sign-up

Add the API key to your environment: `export LOTR_API_ACCESS_KEY='<your-API-access-key>'`


### To test

```
from smannan_lotr_sdk import lotr_api_client

movies, status = lotr_api_client.get_movies()
print (movies)

movies, status = lotr_api_client.get_movies(movie_id='5cd95395de30eff6ebccde56')
print (movies)

quotes, status = lotr_api_client.get_movie_quotes(movie_id='5cd95395de30eff6ebccde5d')
print (quotes)
```