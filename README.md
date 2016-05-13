# FAForever DB project

Contains a dockerfile to run our database in a contained environment, along with tools for managing the database.

# Installation

Get [docker](http://docker.com).

Build the container using

    docker build -t faf-db .

Run using

    docker run -d --name faf-db -e MYSQL_ROOT_PASSWORD=<wanted_password> faf-db

Import Structure

    docker exec -i faf-db mysql -uroot -p<wantedpassword> < db-structure.sql

If you want to execute queries queries and connect to the container try this

    docker exec -ti faf-db mysql -u <username> -p
