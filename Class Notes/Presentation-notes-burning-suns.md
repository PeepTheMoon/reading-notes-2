# My Tech Talk:
It was an interesting project!  We found it difficult to find an API that had the data we were looking for.  We had initially planned our app around finding an API of constellations but found a surprising few.  The closest thing I could find were two graphical simulation planetarums.  

I loved our group's flexibility, ingenuity and humor, because we kept things open and entertained such ideas as a dark humor extinction awareness/calculator app using NASA's Earth Impact Monitoring API to track terrifying, calamity-inducing asteroids over the next 100 years. (not to worry, they have a very low probability of actually making impact, with the most fearful of them all still having a 95.3% chance of missing the Earth.

After some serious digging and tweaking around with my google query parameters, I came across Virtual Sky, which is a browser-based planetarium that allows for customization that can be included in an application via an iframe. This proved to be an exciting addition, as it presents the user with the location of the constellations, the constellation lines and names, displays active meteor showers, and even live updates so that the user sees exactly what's in the sky at given moment.  This can also be manipulated by the user, who can drag the sky projection in the iframe to the direction they're facing.

We decided to supplement that with a weather API which returned an object that included astronomical data like sunset, moonrise, moon phase and moon illumination.  After setting up the API on the backend and testing the endpoints, we found that implementation on the front end yeilded shoddy results, with the astro data not being dependable.
<!-- Get refresher on what wouldn't load from this endpoint -->
We took another turn, employing another API to return the astro data that we wanted.  We also employed the nasa image of the day endpoint to round our the user experience.



## Code Talk:
We were able to use our weather api to search by the city name only, which allowed us to have cleaner url search params, instead of by latitude and longitude.

We ended up using a lot of endpoints, so testing them was an interesting feat due to a perfect storm of technical issues: our heroku backend underwent maintence, our sever was changed, postman has issues with timeouts on working endpoints, and more-- so testing all 24 endpoints took nearly the whole day. One ineretsing problem was with our new API for the astro data: the endpoint is virtually impossible to achieve a passing result result with because values like sun and moon altitude and distance are changing and being updated every moment.