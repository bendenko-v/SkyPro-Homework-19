# SkyPro / Homework 19

REST API with MVC pattern and users authentication.

SQLite database with tables: user, movie, director, genre.

## Usage

Run "app.py" to start the Flask app.

## App features

Authentication is not required for views:
* GET '/users' returns a JSON with all users.
* POST '/users' adds new user to db.
* GET '/users/(id)' returns a JSON with user by id.
* PUT '/users/(id)' changes user data by id.
* POST '/auth' returns a JSON with access_token and refresh_token or 401 Unauthorized.
* PUT '/auth' returns a JSON with refreshed access_token and refresh_token or 401 Unauthorized.

Administrator access authentication (user.role="admin") is required for views:
* DELETE '/users/(id)' delete user by id.

Access authentication is required for views:
* GET '/movies' view returns a JSON with all movies.
* GET '/movies/(id)' view returns a JSON with movie by id.
* GET '/movies?director_id=(id)' view returns a JSON with a list of movies by director id.
* GET '/movies?genre_id=(id)' view returns a JSON with a list of movies by genre id.
* GET '/movies?year=(year)' view returns a JSON with a list of movies by year.
---
* GET '/directors' view returns a JSON with all directors.
* GET '/directors/(id)' view returns a JSON with director by id.
---
* GET '/genres' view returns a JSON with all genres.
* GET '/genres/(id)' view returns a JSON with genre by id.

Administrator access authentication (user.role="admin") is required for views:
* POST/PUT/DELETE '/movies' and '/movies/(id)' views.
* POST/PUT/DELETE '/directors' and '/directors/(id)' views.
* POST/PUT/DELETE '/genres' and '/genres/(id)' views.

