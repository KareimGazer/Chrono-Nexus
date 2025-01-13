# Chrono Nexus

connect time across global horizons by simplifying the complexities of international time zone management.

A production-grade single page app for time zone management.

## Table of content 📋

- [Chrono-Nexus 🌤️](#Chrono-Nexus-️)
  - [Table of content 📋](#table-of-content-)
  - [Features 🚀](#features-)
  - [Future Roadmap 🗺️](#future-roadmap-️)
  - [Getting Started 🚩](#getting-started-)
    - [Locally 🖥️](#locally-️)
      - [Development 👨‍💻](#development-)
      - [Production 🏭](#production-)
    - [Docker 🐋](#docker-)
      - [Development 👨‍💻](#development--1)
      - [Production 🏭](#production--1)
  - [Testing 🧪](#testing-)
    - [Unit Testing 🔎](#unit-testing-)
    - [End-To-End Testing 🎭](#end-to-end-testing-)
  - [Project Structure 📂](#project-structure-)

## Features 🚀

inspired by [world-time-buddy](https://www.worldtimebuddy.com/)

- search
- multi-location

## Future Roadmap 🗺️

- E2E Testing (in progress)
- Vitest
- CI/CD

## Getting Started 🚩

We provide two ways one using docker with minimal setup or locally if you don't get comfortable with containers. both provide production and development environments.

### Locally 🖥️

Start by installing [nodejs](https://nodejs.org/en/learn/getting-started/how-to-install-nodejs)

#### Development 👨‍💻

1. run `npm install` at the root of the project
2. run `npm run dev`

#### Production 🏭

for a production build use

```bash
npm run build
npm run preview
```

### Docker 🐋

start by downloading [Docker](https://www.docker.com/get-started/)

#### Development 👨‍💻

Uses a nodejs container image and runs the app on the vite development server

```bash
docker compose -f .\docker-compose.dev.yml up --build --watch
```

#### Production 🏭

Uses a multi-stage image building process starting from nodejs image to generate the build, and then uses [goStatic](https://github.com/PierreZ/goStatic) image as a static web server built with Go. It's commonly used with the Jamstack although it's an SPA using Vue.

```bash
docker compose up
```

## Testing 🧪

### Unit Testing 🔎

vitest

### End-To-End Testing 🎭


## Project Structure 📂

```
Chrono-Nexus
├── src
├── dist                             static site built files (git ignored)
├── .gitignore                       files to ignore in the VCS
├── .dockerignore                    files to ignroe during docker building process
├── dev.Dockerfile                   Image for running the development server
├── docker-compose.dev.yml           development compose file
├── Dockerfile                       The production container image of the server
├── Dockerfile                       production compose file
└── index.html
```
