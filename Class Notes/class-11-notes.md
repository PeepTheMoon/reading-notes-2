normalizing data:

It's a good idea to separate users out of the data table.

select * from animals, species
where species_id = species.id

STEPS FOR TODAYS LAB:

create new table first, run setupdb to be sure it was made.

have users, resouce and category  Then start modifying them to have a category

npm run setup-db to verify that it went in to the database correctly.  

https://github.com/alchemycodelab/fsjs-foundations-ii-spring-2020/blob/master/curriculum/class-11/demo/server.js for example code on adding the join to the get route.  hit that get route in postman to verify.  same thing for get by id route.  

create new get route that looks up the category that I made. 

https://github.com/dpcairns/animals-full-stack/blob/master/animals/data/create-tables.js

https://github.com/dpcairns/animals-full-stack/blob/master/animals/data/load-seed-data.js

////////////////////////////////////////////////////////

for animal vaccine code example: 
https://github.com/dpcairns/pet-tracker

