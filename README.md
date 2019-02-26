# My Digital Humanities mini project.

# African-American actors in the US movie industry data analysis.
The project idea is to find out african-american actors in the US movie industry status and changes over the years.

# How to use:

* You should have python 3.6.x or higher and pandas library installed.
* wikidata_actor_africanamericans_imdbid.csv and wikidata_filmactor_africanamericans_imdbid.csv were created ahead with wikidata-query service.
* Steps 5 and 6 may take a lot of time because of very large datasets and inefficient implementation.
* Each script file contains instructions for needed files and their location.

1. From IMDb-datasets page (https://www.imdb.com/interfaces/), download files: 
    title.basics.tsv.gz and title.principals.tsv.gz (table columns are described in the link)

2. From Kaggle-The Movies Dataset page (https://www.kaggle.com/rounakbanik/the-movies-dataset), download:
    movies_metadata.csv (table columns are described in the link)
    
3. Download python scripts, wikidata_actor_africanamericans_imdbid.csv and wikidata_filmactor_africanamericans_imdbid.csv files.

4. Run createTitlePrincipalsOnlyActors.py in order to create principals table of only actors records:
title_principals_only_actors.tsv file (which basicly contains imdb_id's of movies and their actors imdb_id's).

5. Run createUsMovies.py in order to create a table of movies produced in the US:
us_movies.csv file (which contains id, title, release year and genres of every movie).

6. Run createYearMoviesMoviesWithAAActors.py
It iterates over the years and for each year, counts the total number of movies produced and the number of those with african-american actors.
Finally writing the requested data to year_movies_moviesWithAAActors.csv file.

7. Run createGenresPopularity.py
It will iterate over all african-american actors from records of wikidata query created files,
and for every actor, find his movies, find movie genres for every movie and add every genre to the genre count.
Finally writing the data to genre_num_of_movies.csv file.

# The final results:
* year_movies_moviesWithAAActors.csv file contains year - number of movies - number of movies with african-american actors (from earliest year in the db to 2018).
* genre_num_of_movies.csv file contains genre - number of movies from this genre (of only movies with african-american actors).

# Final tables and graphs:
These were created manually from the final results files described above.
