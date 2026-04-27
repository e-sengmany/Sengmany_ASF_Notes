# ADVANCED WEB PROGRAMMING - SPRING BOOT

## What is it and why do we care?
- Java Framework
- One stop shop to build a full application
  - handles the "plumbing" so that the different languages can work in tandem to create a application
- Data Requests


## Cyber Security Triad - CIA - Confidentiality, Integriy and Availability
- Availablity - Data is available when it is needed
- Integrity - Ensure that Data is trustworthy, accurate, and has not been tamered with
- Confidentiality - Data is kept secret and accessible only to authorized individuals


## How we make Springboot do things
- Events - URLS and VERBS (GET)
- Event Listeners - What we are waiting to happen
- Event Handlers - What we want to do when the listened for event occurs


# Neon Intake Springboot Demo
1) IntelliJ Springboot Project
  - Dependencies:
    - Spring web
    - Spring data JPA
    - PostGres SQL
    - Flyway Migration
    - Lombok
2) Create docker-compose.yml file in the root directory
   - add the dependencies. Can use this file as an example
3) in terminal run, docker compoose up -d
   - Should appear in the Docker Dashboard
4) Rename application.properties to appllication.yml
   - pulled the data from the announcement.
   - docker-compose tell the structure, application.yml is how to access it
5) Click on database icon on the right
   - new database (postgresql)
   - update: localhost (keep@), port, user, pass, and database (match what is input insize the POSTGRES_DB in the docker yml)
   - test it then apply
6) We create the required tables
   - id and created_at made by db
   - we create all others
7) Create a Class folder in src/main and make a class in that folder
** I did run into the issue with gradle that required me to install packages in order to get past a toolchain error I was receiving in the terminal
    - I did have errors in some of the column names
8) We right clicked the database icon in the class we created. 
   - selected the flyway init option to use the class to create a table in our db.
9) Once that is complete, it will create a V1 (whatever version) file in the db.migration folder (path was determined in our application.yml file)
10) If not already started, runnning ./gradlew bR will run the V1 code and create the table in the db

** What is the difference between docker file and docker compose yaml file?
  - Docker-compose.yaml = multiple instances of different components. server, ports
  - Docker file = if only one file
** What is a port?
  - Door
** Application.yml vs docker-compose.yml 
  - Application = tells the application exactly how we set up our docker
  - Application.properties = does the exact same thing but yml is indentation based
** YAML and YML are the same thing.