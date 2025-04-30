# CatCall

A **microservice-based**, Tinder-style **cat adoption platform** featuring
card-based liking, **location-based recommendations**, and **Dockerized
deployment** using Node.js, React, and MongoDB.

🌐**Live Site:** [https://catcall.zando.dev](https://catcall.zando.dev)

Built with:

- **React** + **Tailwind CSS** (Frontend)
- **Node.js**, **Express**, and **MongoDB** (Backend APIs)
- **Docker Compose** (Deployment)

---

## Run Locally (localhost:3000)

Follow these steps to clone and run the full CatCall app locally.

### 1. Clone the Main Repository

```bash
git clone https://github.com/zandonella/CatCall.git
cd CatCall
```

### 2. Clone the Frontend Repository

Clone this repository into the main repository folder

```bash
git clone https://github.com/zandonella/CatCall-Frontend.git
```

### 3. Clone the Microservice Repositories

CatCall is composed of five microservice backends. Clone each repository into
the main repository folder

```bash
git clone https://github.com/zandonella/cat-database-microservice.git
git clone https://github.com/zandonella/favorites-microservice.git
git clone https://github.com/zandonella/preferences-microservice.git
git clone https://github.com/zandonella/recommender-microservice.git
git clone https://github.com/zandonella/auth-microservice.git
```

| Service                                                                                | Description                     | View API Endpoints                                                        |
| -------------------------------------------------------------------------------------- | ------------------------------- | ------------------------------------------------------------------------- |
| [`CatCall-Frontend`](https://github.com/zandonella/CatCall-Frontend)                   | React frontend                  | –                                                                         |
| [`cat-database-microservice`](https://github.com/zandonella/cat-database-microservice) | Cat data and image storage      | [Link](https://github.com/zandonella/cat-database-microservice#endpoints) |
| [`favorites-microservice`](https://github.com/zandonella/favorites-microservice)       | Manages user favorites/likes    | [Link](https://github.com/zandonella/favorites-microservice#endpoints)    |
| [`preferences-microservice`](https://github.com/zandonella/preferences-microservice)   | Stores user preference settings | [Link](https://github.com/zandonella/preferences-microservice#endpoints)  |
| [`recommender-microservice`](https://github.com/zandonella/recommender-microservice)   | Generates match recommendations | [Link](https://github.com/zandonella/recommender-microservice#endpoints)  |
| [`auth-microservice`](https://github.com/zandonella/auth-microservice)                 | Auth routes                     | [Link](https://github.com/zandonella/auth-microservice#endpoints)         |

> Make sure each service is placed in the directory path expected by
> `docker-compose.yml`.

### 3. Set Up Environment File

While each microservice has its own `.env` file, **only the main repository
requires a `.env` file** to run locally when using Docker Compose from this root
project.

Refer to the `.env.example` file in this repository for the required variables,
then create a `.env` file in the root directory:

```bash
cp .env.example .env
```

Update the values as needed for your local environment.

### 4. Run the App with Docker Compose

```bash
docker-compose up --build
```

Once the services are built and running, visit:

[`http://localhost:3000`](http://localhost:3000)

---
