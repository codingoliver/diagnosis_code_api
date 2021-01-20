# diagnosis_code_api
Backend Take Home Challenge. This project contains RESTful APIS that allows you to utilize an internationally recognized set of diagnosis codes. The APIs allow you to:
* Create a new diagnosis code record
* Edit an existing diagnosis code record
* List diagnosis codes in batches of 20(and paginate through the rest of the record)
* Retrieve diagnosis codes by ID
* Delete diagnosis code by ID

# FUN FACT
* All API endpoints respond within 100ms
* Project includes unit tests for all api endpoints

## Technologies
* Python 3.7
* Django 3
* Django REST FRAMEWORK
* PostgreSQL
* Docker

### Setup
## Installation on Windows, Linux and Mac OS

* [Follow the guide here](https://help.github.com/articles/fork-a-repo) on how to clone or fork a repo

* [Follow the guide here](https://docs.docker.com/docker-for-windows/install/) on how to set up Docker for windows
* [Follow the guide here](https://docs.docker.com/engine/install/ubuntu/) on how to set up Docker for Linux
* [Follow the guide here](https://docs.docker.com/docker-for-mac/install/#:~:text=Install%20and%20run%20Docker%20Desktop,Applications%20folder%20to%20start%20Docker.) on how to set up Docker for Mac OS

* Run project using Docker in simple steps

  ```
  docker-compose up -d --build (Build project docker image and run container)
  
  docker-compose exec web python3 manage.py makemigrations (Make model migrations)
  
  docker-compose exec web python3 manage.py migrate (Migrate models to database)
  
  docker-compose exec web python3 manage.py loaddata diagnosis_codes.json (Load initial fixtures of 4678 diagnosis code records)
  
  ```
* Copy the IP address provided once your server has completed building the site. (It will say something like >> Serving at 127.0.0.1....).
* Open the address in the browser
