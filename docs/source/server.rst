Server
========

Our project uses a HTTP server with express to handle all HTTP requests.

HTTP functions
-----------------

postUser: sends a POST request to save login information in the database

postConfig: sends a POST request to save the desired config to the database

getConfigs: sends a GET request to fetch all of the saved configs a user has

fetchPart functions: sends a GET request for the appropriate part from the database

checkUser: function to check if a user exists in the database