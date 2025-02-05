# 9-gigifty-shared

Why do we need a helper library? 
To avoid duplicate codes accross microservices

- Helpers consist of interfaces that come from all microservices.
- Cloudinary upload methods that will be used to upload images.
- Error handlers
- The API gateway middleware will contain a token that contains a value that the microservice will check to see if it contains a particular value that it requires, or for the microservices to check if the request is actually coming from the API gateway.
- Logger methods
- Helper methods