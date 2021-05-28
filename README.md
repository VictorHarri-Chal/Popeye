# popeye
A basic application (similar to a strawpoll) to learn how Docker works

<!-- ABOUT THE PROJECT -->
## About The Project
The goal of this project is to containerize and define the deployment of a simple web poll application

There are five elements constituting the application:

- **Poll**, a flask Python web application that gathers votes and push them into a `Redis` queue.

- **Redis**, which holds the votes sent by the Poll application, awaiting for them to be consumed by the `Worker`.

- **Worker**, a java application which consumes the votes being in the Redis queue, and stores them into a `PostgreSQL` database

- **PostgreSQL database**, which (persistently) stores the votes stored by the Worker.

- **Result**, a Node.js web application that fetches the votes from the database and displays the result

### Built With
* Docker-compose

<!-- GETTING STARTED -->
## Getting Started

Clone the repositorie and buil images with Docker-compose
```sh
docker-compose up --build
```
see Poll on `localhost:5000/` and Result on `localhost:5001/`

Do not forget to down containers
```sh
docker-compose down -v
```
