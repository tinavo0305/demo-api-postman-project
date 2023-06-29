# api-postman
## Introduction
<br /> This project is used to demonstrate my expertise in REST API testing using Postman.

<br /> **Description:** 
<br />  - Use Postman to build an end-to-end API testing flow for Trello application
<br />  - Write tests with JavaScript for each request to check that the request performed as expected.
<br />  - Create a collection in Postman to store all the requests and make the test run manually or automatically
<br />  - Using Newman to run the test in the command-line interface 

<br /> *Test flow:*
1. Use POST request to create a new board
2. Use PUT request to update the name of the board
3. Use GET request to view the board
4. Use DELETE request to delete the board
5. Use GET request to check the board does not exist
Please follow the [link](https://docs.google.com/spreadsheets/d/1WRHBKVxvaHdh-9NkFGlye0-qPGQdK5_DmP-fpAb5FK4/edit?usp=sharing) for more details 
## How to run the test from Postman app with collection runner
1. Install Postman app
2. Download the file [demo-api-trello.json](https://github.com/tinavo0305/demo-api-postman-project/blob/main/demo-api-trello.json) can be found in this project
3. Import the json file to Postman app to create a collection having all the requests
4. Register a Trello account (if you don't have it yet), if you already have a Trello account, generate key and token from this [link](https://trello.com/app-key)
5. Add key and token as global variables in the Postman app
6. Inside the collection, click *Run* button to execute the test manually or schedule a test run automatically
## Run the test from the command line with Newman
1. Install Newman `npm install -g newman` (remember to install Node.js to use npm)
2. Download the file [demo-api-trello.json](https://github.com/tinavo0305/demo-api-postman-project/blob/main/demo-api-trello.json) can be found in this project
3. Run the collection using the command `newman run demo-api-trello.json --global-var key=[your Trello key] --global-var token= [your Trello token] --global-var TrelloUrl="https://api.trello.com"`
## Create test report 
1. 


