# NAV MTL Backend

NAV MTL is a parking-assistance application built to help drivers navigate Montréal parking restrictions.

This repository contains the **backend API** of the project. The original Android frontend is no longer available in this repository, but the GIF below demonstrates the application in use.

![ezgif com-video-to-gif](https://github.com/MarvensChery/NavMtl-Backend/assets/104527699/8a02cd79-7363-4aca-bad8-609432711d8b)

## Features

The backend supported features including:

* User authentication with JWT
* User profiles
* Parking history
* Favorite locations
* Parking alerts
* User settings
* Friend requests and friendships
* User location data
* Communication with the NAV MTL Android application

## Tech Stack

### Backend

* Node.js
* Express.js
* JavaScript

### Database

* Microsoft SQL Server
* Knex.js

### Authentication & Security

* JSON Web Tokens (JWT)
* bcrypt
* dotenv
* express-validator

### Development Tools

* ESLint
* Airbnb JavaScript Style Guide

## Architecture

```text
Android Application
        |
        | HTTP / REST
        v
Node.js + Express API
        |
        v
Microsoft SQL Server
```

The Android application communicated with the backend through REST API endpoints for authentication, user data, saved locations, parking history, alerts, and social features.

## Database

The backend uses Microsoft SQL Server and includes tables for:

* `utilisateur`
* `favoris`
* `history`
* `parametre`
* `alerte`
* `friend`
* `demandeAmis`
* `friendship`

Relationships between users, favorites, history, alerts, and friendships are maintained using foreign keys.

## Installation

Clone the repository:

```bash
git clone https://github.com/MarvensChery/NavMtl-Backend.git
cd NavMtl-Backend
```

Install dependencies:

```bash
npm install
```

Create a `.env` file and configure the required environment variables for the database connection and JWT authentication.

Then start the server:

```bash
npm start
```

## Linting

Run ESLint and automatically fix supported issues:

```bash
npm run lint
```

## Main Dependencies

* `express`
* `mssql`
* `knex`
* `jsonwebtoken`
* `bcrypt`
* `express-validator`
* `dotenv`
* `cors`

## Project Context

NAV MTL was developed as a collaborative software project.

The complete application originally included an Android frontend with an interactive map and parking-related functionality. This repository preserves the backend portion of the project.

## Authors

**Marvens Chery**

* [LinkedIn](https://www.linkedin.com/in/marvenschery/)
* [GitHub](https://github.com/MarvensChery)

**Christopher Trang**

* [GitHub](https://github.com/christrang)

## Security

Sensitive configuration such as database credentials and JWT secrets should be stored in environment variables and must not be committed to the repository.
