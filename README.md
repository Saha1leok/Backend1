# Backend1
Project description
This project is a simple backend application created using Node.js and Express.
It implements a basic CRUD API (Create, Read, Update, Delete) to work with objects.
All data is stored locally in a data.json file, without using a database.
How to install dependencies
Make sure Node.js is installed on your computer.
Open a terminal in the project folder.
Run the following command:
npm install
This command installs all required dependencies, mainly Express.
How to run the server
Open a terminal in the project folder.
Start the server using:
node server.js
If everything works correctly, the console will show:
Server started on port 3000
List of API routes
Demo routes
GET / – checks if the server is running
GET /hello – returns a hello message
GET /time – returns the current server time
GET /status – returns server status
CRUD routes
GET /objects – get all objects
POST /objects – create a new object
PUT /objects/:id – update an object by id
DELETE /objects/:id – delete an object by id
Example Postman requests
GET all objects
Method: GET
URL:
http://localhost:3000/objects
POST a new object
Method: POST
URL:
http://localhost:3000/objects
Body (raw → JSON):
{
  "name": "Buy milk"
}
PUT update an object
Method: PUT
URL:
http://localhost:3000/objects/{id}
Body (raw → JSON):
{
  "name": "Buy bread"
}
DELETE an object
Method: DELETE
URL:
http://localhost:3000/objects/{id}
Notes
All API routes were tested using Postman.
Data is automatically saved and updated in the data.json file.
This project demonstrates basic REST API principles using Express.
