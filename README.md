# DevOps Capstone Project - IBM
![Build Status](https://github.com/opsabarsec/devops-capstone-project/actions/workflows/ci-build.yaml/badge.svg)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Python 3.9](https://img.shields.io/badge/Python-3.9-green.svg)](https://shields.io/)

This repository contains code for the project in [**IBM-CD0285EN-SkillsNetwork DevOps Capstone Project**](https://www.coursera.org/learn/devops-capstone-project?specialization=devops-and-software-engineering) 
The DevOps capstone project, concludes the 14 modules series for the certification. 

[**IBM DevOps and Software Engineering Professional Certificate**](https://www.coursera.org/professional-certificates/devops-and-software-engineering)

This capstone project brings it all together. From coding and testing to building images and deploying to OpenShift.


As for the other exercises in the previous certification modules, all has been completed using VSCode running on a virtual machine. 

Tasks were designed (course week 1) for 3 springs using a KANBAN board that is shared through

[ZenHub](https://www.zenhub.com/)

## Project layout

The code for the microservice is contained in the `service` package. All of the test are in the `tests` folder. The code follows the **Model-View-Controller** pattern with all of the database code and business logic in the model (`models.py`), and all of the RESTful routing on the controller (`routes.py`).

```text
├── service         <- microservice package
│   ├── common/     <- common log and error handlers
│   ├── config.py   <- Flask configuration object
│   ├── models.py   <- code for the persistent model
│   └── routes.py   <- code for the REST API routes
├── setup.cfg       <- tools setup config
└── tests                       <- folder for all of the tests
    ├── factories.py            <- test factories
    ├── test_cli_commands.py    <- CLI tests
    ├── test_models.py          <- model unit tests
    └── test_routes.py          <- route unit tests
```

## TASKS

Sprint 1: develop a RESTful microservice using good test driven development techniques
Implementation of REST API's for `READ`, `UPDATE`, `DELETE`, and `LIST` while maintaining **95%** code coverage. In true **Test Driven Development** fashion, during the project first you write tests for the code you "wish you had" in test_routes.py, and then the code to make them pass in routes.py . (week 2)

Sprint 2: 
- add continuous integration to the repository in the form of GitHub Actions so that every pull request you make will be fully tested, and code coverage will be measured to ensure that the code maintains high quality. 
- add good security practices to your code to minimize the risk of vulnerabilities and to make sure that those shiny new GitHub Actions are working properly. (week 3)

Sprint 3: 
- build a Docker image and deploy your microservice to Kubernetes manually, creating YAML manifests (week 4)
- develop a continuous delivery pipeline using Tekton, which builds a container image and deploys it to OpenShift using your YAML manifests. (week 5)




