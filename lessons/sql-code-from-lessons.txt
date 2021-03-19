This file contains examples of the SQL code that I have learned and applied in the Coursera's course "Databases and SQL for Data Science with Python".

###########
# Content #
###########
- Statements: COUNT, DISTINCT, LIMIT, SELECT


##############
# Statements #
##############
(Using SanFranciscoFilmLocations Database):

COUNT & WHERE
	- SELECT COUNT(*) FROM FilmLocations;
	- SELECT COUNT(Locations) from FilmLocations WHERE Writer = "James Cameron";
	- SELECT COUNT(*) FROM FilmLocations WHERE ReleaseYear < 1950;

DISTINCT & WHERE
	- SELECT DISTINCT Title FROM FilmLocations;
	- SELECT COUNT(DISTINCT ReleaseYear) FROM FilmLocations WHERE ProductionCompany = "Warner Bros. Pictures";
	- SELECT DISTINCT Title, ReleaseYear from FilmLocations WHERE ReleaseYear >= 2001;
	- SELECT COUNT(DISTINCT Distributor) FROM FilmLocations WHERE Actor1 = "Clint Eastwood";

LIMIT & OFFSET
	- SELECT * FROM FilmLocations LIMIT 25;
	- SELECT * FROM FilmLocations LIMIT 15 OFFSET 10;
	- SELECT DISTINCT Title FROM FilmLocations LIMIT 50;
	- SELECT DISTINCT Title FROM FilmLocations WHERE ReleaseYear = 2015 LIMIT 10;
	- SELECT DISTINCT Title FROM FilmLocations WHERE ReleaseYear = 2015 LIMIT 3 OFFSET 5;

SELECT & WHERE 
	- SELECT * FROM FilmLocations;
	- SELECT Title, Director, Writer FROM FilmLocations;
	- SELECT Title, ReleaseYear, Locations FROM FilmLocations WHERE ReleaseYear>=2001;
	- SELECT Title, ProductionCompany, Locations, ReleaseYear FROM FilmLocations WHERE Writer<>"James Cameron";
	