### Authorization

Users need an API key to use the SDK. They are required to set sign up and acquire their own API keys then set the keys in their system environment before using the SDK.


### HTTP services

An http service module is used to make get requests on behalf of other modules in the SDK. The service grabs the users API key from the system environment, adds it to the request header, and adds query parameters. The HTTP service will respond back to the caller with the HTTP status code and json response.

### Data models

The raw json response is not returned back to the client but instead parsed data models containing Movie and Quote information. This abstracts the low-level data representation of the json away from the user.

### API client

An API client interacts with the HTTP service and data models to make requests for movies and quotes. The client will return a list of valid movies and quotes if successful otherwise an empty list and the error message. The endpoints to get all movies and/or one movie were combined into a single method for the user.