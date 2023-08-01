# API testing with Postman  <img src="https://voyager.postman.com/logo/postman-logo-icon-orange.svg" title="Postman" alt="Postman" width="35" height="35"/> <img src="https://github.com/devicons/devicon/blob/master/icons/javascript/javascript-original.svg" title="JavaScript" alt="JavaScript" width="35" height="35"/>
## Introduction
This project is used to demonstrate my expertise in **REST API** testing using **Postman**.

**Description:** 
- Use Postman to build an end-to-end API testing flow for Trello application
- Write tests with **JavaScript** for each request to check that the request performed as expected.
- Create a collection in Postman to store all the requests and make the test run manually or automatically
- Using Newman to run the test in the command-line interface (CLI)
- Create **test report** with htmlextra

**Test flow:** 
This is an e2e test flow to create, update, view and delete a board in Trello application. The test flow contains the following test case 
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
   
<img width="686" alt="image" src="https://github.com/tinavo0305/demo-api-postman-project/assets/70987579/0edc6d2d-7c0b-4d9c-9653-711da51c1ac3">

<img width="680" alt="image" src="https://github.com/tinavo0305/demo-api-postman-project/assets/70987579/1872b472-48fe-4ef9-8b2b-0baa8b18dd6b">


