# 06 – DevOps : Docker

The project consists of creating a web application using PHP (here Laravel) and a front-end framework (here VueJS) to list and add Picard distributors. The application is orchestrated with Docker, using Docker Compose, and include a database.

The project allow easy import of initial data via a volume.

The following documentation includes instructions for building and running the containers.

## Prerequisites

-   [Docker Desktop](https://www.docker.com/products/docker-desktop/) (for Windows & macOS)
-   [Docker Engine](https://docs.docker.com/engine/) (for Linux)
-   [Node.js](https://nodejs.org/)
-   [npm](https://www.npmjs.com/)
-   [Composer]()

## Installation & Local development

Clone the Git Repository :

```bash
git clone <b3-rattrapages-ehrsam-lucie>

cd <b3-rattrapages-ehrsam-lucie/06-DevOps>
```

Create an .env file from the example .env.example file and adjust the environment variables if necessary.

Install front-end dependencies :

```bash
cd front-end

npm install

cd ..
```

Starting Containers with Docker Compose :

```bash
docker-compose up --build
```

If the volume for the initial data is configured, Docker will handle this step automatically. Otherwise, run the import script manually inside the container.

Open your browser and go to http://localhost:8000 to access the application.

## Features

-   Distributor List: Displays all installed Picard distributors in a list.
-   Add Form: Allows adding new distributors via a simple form.
-   Database: Stores distributor information and allows their management.



## Explicative Video

-   [Video]()

## Helpers

-   [w3schools](https://www.w3schools.com/)
-   [StackOverflow](https://stackoverflow.com/)
-   [Docker Docs](https://docs.docker.com/guides)
-   [Laravel Docs](https://laravel.com/docs/)
-   [Vue3 Docs](https://vuejs.org/guide/introduction.html)
-   Replay of course videos
