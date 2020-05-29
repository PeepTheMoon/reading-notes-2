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
I helped conceptualize the seed of the overall app.  We all researched APIs, and we couldn't find one to suit our needs.  We spitballed several other options based on the APIs we were researching and had a few options to branch off from our seed plan.Later I did some digging and found a slew of options we could take from the seed branches.  I  did some deeper digging and found some ways around the problem through 3 different websites which could suit our needs and allow us to make the seed version of our app.  I also made suggestions for other features we could add, like a link to a dark sites map so users could find the darkest places to watch celestial events, but we focused elsewhere.  We ended up choosing the Virtual Sky option and included it as an iframe.  I also helped research weather endpoints that would return astronomical data as well that could be useful for our app.  