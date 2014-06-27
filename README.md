# Movies GraphGist

Resources: 

http://docs.neo4j.org/chunked/stable/query-load-csv.html

http://docs.neo4j.org/chunked/stable/cypherdoc-movie-database.html

Things that happen in the website:


MATCH (a:Movie)-[:HAS_GENRE]-(b:Genre) RETURN a.id, as movieID, genreID
Person	ACTED_IN	Movie


TODO:

Update graph.db, there's extra stuff in it


movies
MATCH (n:Movie) RETURN n.id as id, n.title as title, n.released as released, n.tagline as tagline, n.summary as summary, .rated as rated, n.duration as duration

MATCH (a:Movie)-[:HAS_GENRE]-(b:Genre) RETURN a.id, as movieID, genreID

person
MATCH (a:Person) RETURN a.id as id, n.name as name, n.born as born

acted in

match (p:Person)-[:ACTED_IN]-(m:Movie) RETURN n.name as Person, m.name as Movie