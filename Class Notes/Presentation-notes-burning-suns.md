# My intro:  
I'm Rachel, a lover of all things space related.  I was drawn to this project because of it's utility in the Pacific Northwest.  I miss the stars when they're constantly being obscured by light pollution and cloud cover.

## User Story
As city goers we don't always have the ability to witness celestial events in the same way as rural residents.  We wanted to be able to see what's going on in the night sky even if we can't actually SEE it.  We made this app for star-gazers, planet watchers, and meteor-shower goers who want to be able to observe the celestial happenings anywhere in the world and from any angle.

### My  Talk:
This was a challenging, interesting project that was really fun to make!  We found it difficult to find an API that had the data we were looking for.  We had initially planned our app around finding an API of constellations but the closest thing I could find were two graphical simulation planetarums.  

After some serious digging I came across Virtual Sky, which is a browser-based planetarium. This proved to be an exciting addition, as it presents the user with the location of the constellations complete with their lines and names, displays active meteor showers, and even live updates so that the user sees exactly what's in the sky at any given moment.  This can also be manipulated by the user, who can drag the sky projection in the iframe to the direction they're facing.
<!-- Show iframe on front end -->

We decided to supplement that with a weather API which returned an object that included astronomical data like sunset, moonrise, moon phase and moon illumination to give the user more data for planning their stargazing excursions.
<!-- Show both weather endpoints -->
  After setting up the API on the backend and testing the endpoints, we found that implementation on the front end yeilded shoddy results, with the astro data not being dependable. It had to be accessed through a date string which was another layer of complexity for retrieveing the data. We took another turn, employing another API to return the astro data that we wanted, which isn't very consistent either.

#### Code Talk:
We were able to use our weather api to search by the city name only instead of by latitude and longitude, which allowed us to have cleaner url search params. 
<!-- Show URL in deployed site and location endpoint on BE -->

We also had the idea of including a feature to allow users to take notes and even make wishes, so we set up a boolean on our notes chart and even found a cool button icon from the material-ui library to employ a star instead of a checkbox when the user designates a wish.
<!-- Show the create tables file -->
<!-- Show endppoint and joins -->

One interesting problem was with testing our new API endpoint for the astro data: the endpoint is virtually impossible to achieve a passing result result with because values like sun and moon altitude and distance are changing and being updated every moment.  
<!-- Show test in postman -->

##### Some things we wanted to add, but chose to focus elsewhere:
1. A calendar to save dates of celestial events important to the user.

2. A link to a dark sites map so the user can find the darkest places nearby to view the celestial events.

Fun points:
I loved our group's flexibility and ingenuity. We kept things open and entertained such ideas as a dark humor extinction awareness app using NASA's Earth Impact Monitoring API to track terrifying, calamity-inducing asteroids over the next 100 years, and even a life-on-Mars weather app.

###### Individual Contributions 

-Questions:
Overall Contributions
What contributions did you personally make? Please describe all of your contributions (e.g., artwork, videography, animations, layout, fontography and other styling, HTML structure, JS for DOM manipulation, JS logic, localStorage, Google API, AJAX/JSON, etc.).

Code Contributions
Provide a link to your project's commit graph (or equivalent) for anything else you'd like to highlight (e.g., features, README.md, automated tests, test documents, tasks described in GitHub issues, etc).

Collaboration Contributions
Describe how you collaborated with your team throughout the development process (e.g., addressed issues assigned on GitHub, coordinated meetings with team, etc.).

-Answers:
1. Link to our planning: https://miro.com/app/board/o9J_ksGGC_8=/
I helped conceptualize the seed idea of the overall app as a location-based stargazing app.  I started the Miro board where I took down notes for what we wanted our MVP to look like given we could find a constellations API. 

We all researched APIs, and we couldn't find one to suit our needs.  We spitballed several other options based on the APIs we were researching and had a few options to branch off from our seed plan and I recorded those in Miro along with the API's that could be utilized.  

I did some deeper digging and found some ways around the problem through 3 different websites which could suit the needs of our original app idea and allow us to make the seed version of our app.  I added notes in Miro. I also made suggestions for other features we could add, like a link to a dark sites map so users could find the darkest places to watch celestial events, but we focused elsewhere.  We ended up choosing the Virtual Sky option after looking over the resources in Miro as a group and decided to include it as an iframe.  I also helped research weather endpoints that would return astronomical data as well that could be useful for our app. 

In Miro I did the wireframe for mobile and we discussed that it could translate fairly easily into wider screens.  I also did a mind map in Miro for the project ideas/features we discussed implementing.  As a group we helped discuss, write, and divide up tickets in Miro kanban.  You can only assign each ticket to one person, so we tried to fairly divide up the work when we pair programmed.  

On Monday the 18th I started the backend repo, added initial table data and data files, along with renaming of files where needed.  I also set up the postgres server and tested for connectivity in postman and PGAdmin.  On Tuesday the 19th I did some merging of changes Langston had made while troubleshooting the back end and resolved merge conflicts.  I fixed some bugs with the database setup, and Melissa and I pair programmed some of the backend API endpoints and tested in postman.  We updated where needed and added authorization. We also paired on the search and detail pages for the front end.  We had to do a lot of research on working with material-ui at this stage so there was a lot of fun problem solving with new solutions and learning how to work with state when using functional components.  We also made successful API calls to the weather's locaton endpoint on the backend and wrote logic for getting the city from the search params to the details page.

On the 20th I updated the routes to the pages on app.js on the front end.  Melissa and I did a bit more pairing on the front end for the details page and then I went to finish up the back end where I updated the saved-locations endpoint and added a post and delete route for the saved-locations endpoint, tested in postman and PGAdmin.  I also updated our tables to remove some unused data from the saved-locations table, updated the data in the post route, and added notes for the endpoints.  I updated our journals table, renamed it as notes table and updated all corresponding files, as well as adding the get all, get one, post, put and delete routes for notes.  I tested and verified them all in postman and PGdmin.  I also added the nasa picture of the day endpoint and tested in postman.

On the 21st I worked on the backend more, editing the notes table to increase the character count, added and tested a new endpoint for astro data from another API to try and supplement the unreliability of our previous endpoint for sun and moon data.  I added try/catch syntax to all endpoints to allow for error messages and tested them.  I also had to update our server to a new server, added an endpoint to delete ONE saved location (on the backend the delete endpoint deleted all saved locations when tested in postman, but after adding the new delete endpoint and testing it for one, it turns out on the front end the original one didn't delete all.  Very interesting!).  I repaired the get one note endpoint.  I also ran tests for all 12 endpoints for both with and without authorization in postman and added screenshots to the repo.  On the front end I paired with Langston to do some styling on the details page.  We did a lot of reading and trying things as we were all new to working with styling using material ui and their color palettes.  It was interesting to see what we could target and change and what we could not.  We discussed as a group what areas of the app each of us woud talk about.

On the 22nd I added notes on the backend and I cleaned up the code for the front end.  I also composed a user story for our app.  I wrote down my piece of the presentation and we practiced it as a group a couple of times.  

https://github.com/langstonBS/burning-suns-fr/commits/master?before=835a11204ca0af001bb57cd87a95af1f132288eb+35
commit history for front end, all

https://github.com/langstonBS/burning-suns-fr/commits?author=PeepTheMoon
commit history for front end, mine only

https://github.com/PeepTheMoon/burning-suns-be/commits/master
commit history for backend, all

https://github.com/PeepTheMoon/burning-suns-be/commits?author=PeepTheMoon
Commit history for backend, mine only


Our team collaborated through the entire process.  We discussed how we would approach taska and any issues.  We discussed the direction of our app should we not be able to find a constellations API.  I got insight and made sure to get approval for each of the things I did in Miro, like what browser-based planetarium we should use, features to include like a calendar (which Nikki wrote logic for but then removed after we discussed its current utility as a group), and the appearance of the wireframes.  We all helped wrote and divide up tickets.  We met for a stand up every morning and talked about what was important for that day and who would work on it.  We reconveined usually mid day and also at the end of every day to do merging of pull requests together, walk throught he functionality together, and talk about what we still needed to do the following day.  Occasionally we stayed after hours and discussed what we would be working on.  We also got help from eachother if we needed a second pair of eyes, someone to troubleshoot or debug with, etc.  We also stayed in communication about different approaches we were going to take as they happened and discussed the technical issues so everyone would know, like when Nikki's power went out or my postman started timing out on retrieving data from endpoints that were tested to work, or my computer crashing several times (chrome is a bit too taxing for my little granny macbook).  We also made sure to go through the user experience of the app together, talk about features we wanted to add or change, and talked about styling and which color palettes to use as a group.  It was a very collaborative, democratic process and I loved working with everyone.  This was surprisingly stress free considering we all were learning material-ui together for this project.  