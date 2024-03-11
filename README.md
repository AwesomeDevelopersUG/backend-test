# Test assignment: Backend
Use whatever language/framework you prefer (we mostly use Python and Kotlin).
## 1. Setup an environment
To complete the assignment you will need a running PostgreSQL and Redis instances. So, as a first step, please, create a `docker-compose.yml` file that will spin up those databases for you. Make sure that you will be able to connect to them from your future server.
Within PostgreSQL, create a new database (you can name it as you wish) and a new table `users`. Each row of the table, unsurprisingly, would represent a user of some website and should contain the following information:
* *Name*
* *Registered at*  - timestamp when user was registered
As long as table is able to represent the two fields mentioned above, the table can be defined any way you prefer.
## 2. Implement a simple server to serve a SQL query
As the core of the task, we would like you to write a SQL query that would operate on PostgreSQL database table you have created in the previous step.
```
Write a SQL query that will return the numbers of new user registrations per month for the past year to date except current month (e.i. in date range [(now - 12 months), beginning of current month)). Don't forget to include months with no registrations.
```
## 3. Implement the HTTP Server
Using a language and/or a framework of your choice, create an HTTP endpoint that will serve results of the query from the previous step as JSON output.
## 4. Add caching
The output of the SQL query doest not change that often, so it would make sense to cache its results.
* Implement caching via Redis for results of your newly created query.
* Make sure that cache is invalidated on time and endpoint does not return stale results.
* Try adding caching in a way that would minimize the amount of change in the existing code.

## What we expect from you

* `docker-compose.yml` file to run required services
* README file that will describe how run the project (including DB setup)
* source code of the server

include all of these in an archive and send it to jobs@awesomedevelopers
