🚀 Node.js Express CRUD API
This is a lightweight backend application built with Node.js and Express. It implements a basic RESTful API to manage objects using standard CRUD (Create, Read, Update, Delete) principles without the need for a complex database.

📋 Project Overview
Backend: Node.js & Express.
Storage: Local data.json file (NoSQL style).
Functionality: Full CRUD operations and server diagnostic routes.
🛠 Installation & Setup
1. Install Dependencies
Ensure you have Node.js installed on your machine. Open your terminal in the project root folder and run:

Bash
npm install
This command installs all necessary packages, primarily Express.

2. Run the Server
Start the application by running:

Bash
node server.js
Upon a successful start, the console will display:

Server started on port 3000

📡 API Routes
Demo & Diagnostic Routes
Method	Route	Description
GET	/	Health check to see if the server is live
GET	/hello	Returns a friendly greeting message
GET	/time	Returns the current server timestamp
GET	/status	Returns the current operational status
CRUD Operations
Method	Route	Description
GET	/objects	Retrieve a list of all stored objects
POST	/objects	Create and save a new object
PUT	/objects/:id	Update an existing object by its unique ID
DELETE	/objects/:id	Remove an object from the storage by its ID
📮 Postman Testing Examples
1. Fetch All Objects
Method: GET
URL: http://localhost:3000/objects
2. Create a New Object
Method: POST
URL: http://localhost:3000/objects
Body (raw → JSON):
JSON
{
  "name": "Buy milk"
}
3. Update an Object
Method: PUT
URL: http://localhost:3000/objects/{id}
Body (raw → JSON):
JSON
{
  "name": "Buy bread"
}
4. Delete an Object
Method: DELETE
URL: http://localhost:3000/objects/{id}
📝 Technical Notes
Data Persistence: All changes are automatically synchronized with the data.json file.
Testing: All routes have been verified using Postman.
Educational Value: This project serves as a practical demonstration of REST API architecture using the Express framework.
