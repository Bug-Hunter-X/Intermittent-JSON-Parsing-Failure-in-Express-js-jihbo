# Intermittent JSON Parsing Failure in Express.js

This repository demonstrates a bug in an Express.js application where JSON payload parsing intermittently fails. The `express.json()` middleware appears to work correctly in most cases but unexpectedly fails for some requests, resulting in an empty `req.body`.

## Bug Description

The application is designed to receive JSON data via a POST request to the `/data` endpoint.  The `express.json()` middleware is used to parse the incoming JSON.  However, the application logs an empty `req.body` for some requests, even when the request body is correctly formatted.

## Reproduction Steps

1. Clone this repository.
2. Run `npm install` to install the dependencies.
3. Run `node bug.js` to start the server.
4. Send POST requests to `http://localhost:3000/data` with a JSON payload using tools like Postman or curl.  Observe that some requests might log an empty object to the console despite having a valid JSON payload.

## Solution

A solution and explanation can be found in `bugSolution.js`.