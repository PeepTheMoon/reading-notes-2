normalizing data:

It's a good idea to separate users out of the data table.

select * from animals, species
where species_id = species.id