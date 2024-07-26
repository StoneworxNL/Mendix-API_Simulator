## Mendix API Simulator

API Simulator allows you to generate dynamic responses for HTTP requests, so you can test consumed API's without any dependencies.

Most consumed API's are not a simple 'fire and forget'. API Responses will be processed, shown on a page or combined with other API calls in complex use cases. Unfortunately, I have been in situations where it is not possible to properly test the logic surrounding consumed API's, for example:

-It is still in development, so all you have is the API structure.
-Getting access to the API requires a lengthy intake and approval phase
-The API is available, but there is no test/staging environment (or the test environment has poor data quality)
-Firewalls/restrictions require deployment of the application to call the API, local testing is not possible
-You want to test the handling of exceptional scenarios before they occur, for example rate limiting (HTTP 429 Too Many Requests)

You can run the API simulator as part of your Mendix app or in a separate app based on your preference. 

## Dependencies
-CommunityCommons

## Key features
-Configure relative endpoints up to 5 levels deep.
-Supports the following HTTP methods: GET, POST, PUT, DELETE.
-Configure multiple response templates for each layer and supported HTTP Method.
-Supports variables in response templates to generate dynamic contents for responses.
-Extensible: define custom microflow to generate a response or select a specific response template.
-Export/Import endpoint configurations
-Debugger: pause incoming requests, allowing you to edit the synchronous response before it is returned to the consuming application
-Supports dynamic paths (e.g. a unique id).

## Usage
1. Connect your developer/administrator user role to the Developer module role
2. Connect the "IncomingRequest_Overview" page to your navigation
3. Start by sending HTTP requests to <http(s)://yourappurl>/rest/apisimulator/<anypath>

Note: More documentation can be found in the "Documentation" tab which is available on the aforementioned landing page

## Demo
https://stoneworx-api-simulator-sandbox.mxapps.io/index.html?profile=Responsive

NOTE: Do not use for/connect to production environments. If you send any data to the demo endpoint it will be stored and publicly available until the "Delete All" button is clicked!
Side note: if the overview is empty because someone did use the "Delete all" button, use the "Run demo" button to restore the demo data

## Issues, suggestions and feature requests
https://github.com/StoneworxNL/Mendix-API_Simulator/issues

