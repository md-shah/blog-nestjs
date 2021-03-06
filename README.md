# Blog Backend based on NestJS & PostgreSQL
[![Build Status](https://api.travis-ci.com/md-shah/blog-nestjs.svg?branch=master&status=passed)](https://travis-ci.org/md-shah/blog-nestjs)

This is Blog-Backend repository built on NestJS with a scalable architecture and almost all industry standards. I am developing this project as a reference/starter kit for further upcoming projects. Since the projects that I worked in my career life is some what not scalable or having issues in the longer run.

---

### Getting started

Build docker for the particular env and run container

##### Development Environment:
We are Application in Watch Mode with Debugger.

```sh
$ docker-compose --env-file ./src/server/environments/.development.env -f docker-compose.yml build app-dev
$ docker-compose --env-file ./src/server/environments/.development.env -f docker-compose.yml up app-dev

( To run containers in the background: use "-d" in the above up command )
```

##### Production Environment:
After generating 'dist' build, We run the artifacts from dist folder.

```sh
$ docker-compose --env-file ./src/server/environments/.production.env -f docker-compose.yml build app-prod
$ docker-compose --env-file ./src/server/environments/.production.env -f docker-compose.yml up app-prod

( To run containers in the background: use "-d" in the above up command )
```

##### Test Environment:
Used to run tests including Linter check and Unit tests.

```sh
$ docker-compose --env-file ./src/server/environments/.test.env -f docker-compose.yml build app-test
$ docker-compose --env-file ./src/server/environments/.test.env -f docker-compose.yml up app-test

( No need to run test in background. Inside CI/CD pipelines, run the up command, 
So we can see the build logs and status [passed or failed] )
```
---

### Todo List - Features

- [x] Setup basic repo && files structuring
- [x] Swagger
- [x] Linter
- [x] Update Git Hooks to check and validate lint, unit test and any console.logs.
- [ ] Show above executions as separate ticks.
- [x] Implement docker based system 
- [ ] Design patterns
- [ ] Generic DB connection option
- [ ] Handle all DB connection scenarios (connecting, connected, error, retry after x secs)
- [ ] Extending error classes for every exception as well rollback feature
- [ ] npm script to generate a module with controller, service, Models & helper functions
- [ ] Add to do here

### Future Todo List

- [ ] Convert this to a microservice based architecture 
- [ ] Add to do here

---

### Special thanks to,

* [Arjun M] - DevOps Knight, Helped me with Docker!

   [Arjun M]: <https://www.linkedin.com/in/arjun-m-704a04104/>
