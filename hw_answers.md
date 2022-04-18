
###MVP

1- What is responsible for defining the routes of the games resource?
    The Router

2- What do you notice about the folder structure? Whats the client responsible for? Whats the server responsible for?
    Client is front-end, server back-end.
    Client is responsible for fetching and displaying the data from the DB and for recieveing new data and passing it back to . 
    Server side is responsible for requesting the data from the DB and psssing on new data from the front-end to the DB through correct routing. 

3 - What are the the responsibilities of server.js?
    server.js sets up the routes for the different HTTP server requests (using the createRouter helper function) and connects to the DB to pull the data required for the api routes. 

4- What are the responsibilities of the gamesRouter?
    gamesRouter calls the helper function createRouter and passes in the games data from the DB. And then it defines the prefix and what routes the app should use => gamesRouter. 

5- What process does the the client (front-end) use to communicate with the server?
    GamesService uses different fetch requests depending on the CRUD action. 


6- What optional second argument does the fetch method take? And what is it used for in this application? Hint: See Using Fetch on the MDN docs
    Second argument is an init object, that provides paraneters and further information to the fetch request. Such as setting the method, GET (default), POST, DELETE, PUT
    Providing futher data (for a post) in a Body and a Header provides additional data to help the server understand the request type.

7- Which of the games API routes does the front-end application consume (i.e. make requests to)?
    Get (find())- get all DB data to be displayed under form.

    Post (insertOne()) - to add a new game, taken the data from the form and posting it to the DB.

    Delete (deleteOne()) - remove the game by id (based on game clicked-> each listed game has a key=game._id)


8- What are we using the MongoDB Driver for?
    Creates a connection to the Mongo DB.