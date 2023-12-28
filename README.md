In this project, let's build an IPL Dashboard App by applying the concepts we have learned till now.

Refer to the image below:

ipl-dashboard-output

Design Files
Click to view
Extra Small (Size < 576px) and Small (Size >= 576px) - Home
Extra Small (Size < 576px) and Small (Size >= 576px) - Team Matches
Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px) - Home
Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px) - Team Matches
Set Up Instructions
Click to view
Download dependencies by running npm install
Start up the app using npm start
Completion Instructions
Functionality to be added

The app must have the following functionalities

When the app is opened, Home Route should be displayed
When the Home Route is opened,
Make HTTP GET request to the teamsApiUrl
loader should be displayed while fetching the data
After fetching the data, the list of teams should be displayed
When a team card in Home Route is clicked,
Page should be navigated to the Team Matches Route with the URL /team-matches/:id
When the Team Matches Route is opened,
Make HTTP GET request to the teamMatchesApiUrl with the team id to get the recent matches data of the team
Example: https://apis.ccbp.in/ipl/KKR
loader should be displayed while fetching the data
After fetching the data, the team banner, latest match, and list of recent matches should be displayed
API Requests & Responses

teamsApiUrl

API: https://apis.ccbp.in/ipl
Method: GET
Description:
Returns a response containing the list of all IPL teams

Response
 
JSON
teamMatchesApiUrl

API: https://apis.ccbp.in/ipl/:id
Example: https://apis.ccbp.in/ipl/KKR
Method: GET
Description:
Returns a response containing details of all recent matches of a team

Response
  
JSON
Components Structure

home component structure

team matches component structure

Implementation Files

Use these files to complete the implementation:

src/App.js
src/components/Home/index.js
src/components/Home/index.css
src/components/TeamCard/index.js
src/components/TeamCard/index.css
src/components/TeamMatches/index.js
src/components/TeamMatches/index.css
src/components/LatestMatch/index.js
src/components/LatestMatch/index.css
src/components/MatchCard/index.js
src/components/MatchCard/index.css
Quick Tips
Click to view

To display the animated loader, we need to import the Loader component using the below statement

In order to display the given animated loader, pass the type and color props to the Loader component with values as Oval and #ffffff , respectively

Important Note
Click to view

The following instructions are required for the tests to pass

The banner image in the Team Matches Route should have the alt attribute value as team banner
The alt attribute values for the images received from the response are given in the Example response
The API responses received from the given api URLs should be converted to camel case
Wrap the Loader component with an HTML container element and add the testid attribute value as loader to it as shown below <div testid="loader"> <Loader type="Oval" color="#ffffff" height={50} width={50} /> </div>
Render HomeRoute component when path in URL matches /
Render TeamMatchesRoute component when path in URL matches /team-matches/:id
No need to use the BrowserRouter in App.js as we have already included in index.js file
Each TeamMatchesRoute should have different gradient colors as background based on the selected team
Resources
Image URLs
https://assets.ccbp.in/frontend/react-js/ipl-dashboard-sm-bg.png
https://assets.ccbp.in/frontend/react-js/ipl-dashboard-lg-bg.png
https://assets.ccbp.in/frontend/react-js/ipl-logo-img.png alt should be ipl logo
Colors

Background Colors:

Hex: #1e293b
Hex: #a4261d
Hex: #5755a7
Hex: #d91c1f
Hex: #f7db00
Hex: #ffffff33
Hex: #da237b
Hex: #13418b
Hex: #f26d22
Hex: #4f5db0
Hex: #0f172a

Border Colors

Hex: #ffffff
Hex: #475569

Text Colors

Hex: #ffffff
Hex: #18ed66
Hex: #e31a1a
Font-families
Bree Serif
Things to Keep in Mind
All components you implement should go in the src/components directory.
Don't change the component folder names as those are the files being imported into the tests.
Do not remove the pre-filled code
Want to quickly review some of the concepts you’ve been learning? Take a look at the Cheat Sheets.
