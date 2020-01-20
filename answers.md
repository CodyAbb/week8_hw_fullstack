### Questions

1. What is responsible for defining the routes of the `games` resource?
gamesRouter (which is a createRouter function) is responsible for setting the routes for the resources.

2. What do you notice about the folder structure?  Whats the client responsible for? Whats the server responsible for?
client folder is responsible for the vue components and rendering any data. Whereas the server folder now houses the functions for querying the database and json api.

3. What are the the responsibilities of server.js?
This file is responsible for connecting to a database 'games_hub' and a collection within that. It also connects to express for the back-end, providing an argument for the router. and starting to listen on the specified port.

4. What are the responsibilities of the `gamesRouter`?
The gamesRouter associates the database with the create_router. This is a helper that follows restful conventions to query the database for CRUD operations.

5. What process does the the client (front-end) use to communicate with the server?
Within the client folders there is a GameService file which contains methods to GET and POST information to the base url of the server. Starts with '/api/games' and then can send payloads of information on the POST.

6. What optional second argument does the `fetch` method take? And what is it used for in this application? Hint: See [Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) on the MDN docs
Fetch takes an init object as its second argument. This object can be used to provide credentials or in this case send data to a POST http.

7. Which of the games API routes does the front-end application consume (i.e. make requests to)?
the get route of '/'

8. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?
driver provides both callback-based and Promise-based interaction with MongoDB

## Extension

Why do we need to use [`ObjectId`](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html) from the MongoDB driver?
This will transfer the object id which is transferred to the client side as a string back into a hex object that can be sent back to the database for querying or update/destroy.

Add to your diagram the dataflow for removing a game.
