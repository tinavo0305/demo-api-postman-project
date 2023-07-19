# API testing with Postman
## Introduction
This project is used to demonstrate my expertise in REST API testing using Postman.

**Description:** 
- Use Postman to build an end-to-end API testing flow for Trello application
- Write tests with JavaScript for each request to check that the request performed as expected.
- Create a collection in Postman to store all the requests and make the test run manually or automatically
- Using Newman to run the test in the command-line interface
- Create test report with htmlextra

**Test flow:**
This is an e2e test flow to create, update, view and delete a board in Trello application 
1. Use POST request to create a new board
2. Use PUT request to update the name of the board
3. Use GET request to view the board
4. Use DELETE request to delete the board
5. Use GET request to check the board does not exist

Please view this [link](https://docs.google.com/spreadsheets/d/1WRHBKVxvaHdh-9NkFGlye0-qPGQdK5_DmP-fpAb5FK4/edit?usp=sharing) for detailed test plan
## How to run the test from Postman app with collection runner
1. Install Postman app
2. Download the file [demo-api-trello.json](https://github.com/tinavo0305/demo-api-postman-project/blob/main/demo-api-trello.json) can be found in this project
3. Import the `demo-api-trello.json` file to Postman app to create a collection having all the requests
4. Register a Trello account (if you don't have it yet), if you already have a Trello account, generate key and token from this [link](https://trello.com/app-key)
5. Add key and token as global variables in the Postman app
6. Inside the collection, click *Run* button to execute the test manually or schedule a test run automatically
## Run the test from the command line with Newman
1. Install Newman `npm install -g newman` (remember to install Node.js to use npm)
2. Download the file [demo-api-trello.json](https://github.com/tinavo0305/demo-api-postman-project/blob/main/demo-api-trello.json) can be found in this project
3. Run the collection using the command `newman run demo-api-trello.json --global-var key=[your Trello key] --global-var token= [your Trello token] --global-var TrelloUrl="https://api.trello.com"`
## Create test report with htmlextra
1. Install htmlextra reporter: `npm install -g newman-reporter-htmlextra`
2. Run the collection using the command `newman run demo-api-trello.json --global-var key=[your Trello key] --global-var token= [your Trello token] --global-var TrelloUrl="https://api.trello.com" --reporters cli,htmlextra`
3. The report will be generated in the *newman* folder which is the same location as postman collection
<img width="557" alt="image" src="https://github.com/tinavo0305/demo-api-postman-project/assets/70987579/789b1925-9cbd-4a0d-9a97-0643983fcc38">
<img width="553" alt="image" src="https://github.com/tinavo0305/demo-api-postman-project/assets/70987579/c97c85ce-8c86-4eb0-bc68-8e5e7b36fa25">



