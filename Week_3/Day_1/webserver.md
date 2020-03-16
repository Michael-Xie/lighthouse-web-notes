# Web Server

Last Week we looked at TCP, now we will look at HTTP from scratch

## TCP Connection
- Can phone
- establish connection between server and client
- someone listens
- someone sends messages
- someone ressponds

## HTTP
- The server listens to requests
- The server also listens on specific *ROUTES* <<<

amazon.com <=== specific route
amazon.com/search/jskldjfkd <== specific route

- The server is stateless <<<

server amnesia - server will never remember, doesn't remember what you are on your second, third etc requests

- Client can make request to a server
- Server will respond with a specific code and data
- Client will receive the response

## Ports
- about 65K
- a port is specific to one service/program
- basic way to connect an app to the internet

## Requests
- almost all web apps allow users to manipulate data in various ways and usually in four categories: 
1. **C**reate: Add a new record
2. **R**ead: Retrieve the value of a record
3. **U**pdate: Update a record's value
4. **D**elete: Delete a record

GET - READ - get something from server
POST - CREATE - make change to something from server
PUT - UPDATE -
DELETE - DELETE

idempotent - multiple identical requests shoudl have teh same effect as a sing request
	- GET, HEAD, OPTIONS, TRACE are idempotent
	- POST is not necessarily idempotent


## Express
- middleware
- routing
- "/" - home
## Tips and Tricks
### html 
``` <%= <var> %> 
```
can write javascript inside

the equal sign to display to play, no equal sign needed for logic
