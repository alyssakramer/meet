Objective
To build a serverless, progressive web application (PWA) with React using a
test-driven development (TDD) technique. The application uses the Google
Calendar API to fetch upcoming events.


As a user
I should be able to “filter events by city”
So that I can see the list of events that take place in that city
SCENARIO 1: WHEN USER HASN’T SEARCHED FOR A CITY, SHOW UPCOMING EVENTS FROM ALL CITIES.
Given user hasn’t searched for any city
When the user opens the app
Then the user should see a list of all upcoming events

SCENARIO 2: USER SHOULD SEE A LIST OF SUGGESTIONS WHEN THEY SEARCH FOR A CITY.
Given the main page is open
When user starts typing in the city textbox
Then the user should see a list of cities (suggestions) that match what they’ve typed

SCENARIO 3: USER CAN SELECT A CITY FROM THE SUGGESTED LIST.
Given the user was typing “Berlin” in the city textbox
And the list of suggested cities is showing
When the user selects a city (e.g., “Berlin, Germany”) from the list
Then their city should be changed to that city (i.e., “Berlin, Germany”)
And the user should receive a list of upcoming events in that city
FEATURE 2: SHOW/HIDE AN EVENT'S DETAILS
As a user, I should be able to expand and hide event details so that I can see the details when needed and collapse them when I don’t. 
•	Scenario 1: An event element is collapsed by default
Given the user searches an event, when the user clicks on an event, the user should see that the event details are collapsed. 
•	Scenario 2: User can expand an event to see its details
•	Given the event details are collapse, when the user press expands details button then the user should see all the details for the event
•	Scenario 3: User can collapse an event to hide its details
Given that a user has expanded the details, when a user no longer wants to see the details, the user should be able to hide the event details with a collapse button

FEATURE 3: SPECIFY NUMBER OF EVENTS
As the user, I should be able to specify the number of events I want to see so that I can narrow or expand the results shown at one time as I please. 

•	Scenario 1: When user hasn’t specified a number, 32 is the default number
Given the user has searched for an event, when the user sees the default number of events listed then the user should see 32 events
•	Scenario 2: User can change the number of events they want to see
Given the user has searched for events, when the  user goes to the specified number of events, then the user should be able to change the number of events listed based on their preferences 

FEATURE 4: USE THE APP WHEN OFFLINE
As the user, I should be able to use the app when offline so that I have this information when there’s no internet connection. 
•	Scenario 1: Show cached data when there’s no internet connection
Given the user has no internet conecctin, when the user searches for events, then the user should see the cached data
•	Scenario 2: Show error when user changes the settings (city, time range)
Given the user has no internet connection, when the user changes the city, then the user should get an error 


FEATURE 5: DATA VISUALIZATION
As the user, I should be able to see a chart with the number of upcoming events so that I have this information readily available. 

•	Scenario 1: Show a chart with the number of upcoming events in each city
Given the user has open the app, when the user goes the chart, then the user should see a chart with the number of upcoming events in each city
