# GamerLand-Service-Layers

Welcome to the GamerLand service layers repository! This repository houses the code that provides the functionality to interact with the GamerLand database. The database is built using MongoDB, a document-based NoSQL database, and contains four collections: Users, Games, Reviews, and Ratings. These collections are structured as per the MVP requirements of the GamerLand web app.

# Data Structures
The data structures for each collection are as follows:

Users (MVP)

{
   "userId": "string",
   "firstName": "string",
   "lastName": "string",
   "email": "string",
   "password": "string",
   "gender": "string",
   "country": "string",
   "createdAt": "string",
   "updatedAt": "string"
}

Games (MVP)

{
   "gameId": "string",
   "title": "string",
   "description": "string",
   "releaseDate": "string",
   "developer": "string",
   "publisher": "string",
   "genre": "string",
   "console": ["string"],
   "imageUrl": "string",
   "createdAt": "string",
   "updatedAt": "string"
}

Reviews (MVP)

{
   "reviewId": "string",
   "userId": "string",
   "gameId": "string",
   "text": "string",
   "rating": "number",
   "createdAt": "string",
   "updatedAt": "string"
}

Ratings (MVP)

{
   "ratingId": "string",
   "userId": "string",
   "gameId": "string",
   "rating": "number",
   "createdAt": "string",
   "updatedAt": "string"
}

The structure for the ratings collection could also be represented in the following format:

{
  "userid": "string",
  "gameid": "string",
  "rating": {
    "value": "integer",
    "max": 10,
    "min": 1
  },
  "comment": "string"
}


In addition to the MVP collections, there are two stretch features that will not be discussed in detail here. These features are Discussions and User Search.


# Implementation Details

The GamerLand database is designed to be flexible and scalable, ensuring that the application can handle high traffic and perform well as the data grows. The use of MongoDB, along with JSON-like documents, allows for efficient management of unstructured data, such as user-generated content, which is an essential part of GamerLand.

The RAWG.io API and OpenVGDB are utilized for game images, descriptions, and other data deemed necessary for the web app.


# Contributing

If you are interested in contributing to this repository, please see the CONTRIBUTING.md file for guidelines on how to get started.


# License

This repository is licensed under the MIT license. Please see the LICENSE file for more information.
