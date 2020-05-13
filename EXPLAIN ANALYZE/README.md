&gt; explain analyze VERBOSE  select actor_id,first_name, last_name,last_update from actor

2. explain analyze VERBOSE  select first_name, last_name from actor where actor.first_name='Nick'

3. explain analyze VERBOSE  select first_name, last_name,last_update 
from actor where actor_id=100
order by first_name,last_name

4. explain analyze VERBOSE 
 select rating, count(film_id)
 from film where film.length >100
 group by rating
 order by rating desc
 
5. explain analyze VERBOSE 
select city.city, country.country from city
 inner join country on city.country_id= country.country_id
