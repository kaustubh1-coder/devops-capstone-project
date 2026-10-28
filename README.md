[![CI Build](https://github.com/kaustubh1-coder/devops-capstone-project/actions/workflows/ci-build.yaml/badge.svg)](https://github.com/kaustubh1-coder/devops-capstone-project/actions)
# DevOps Capstone Template

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Python 3.9](https://img.shields.io/badge/Python-3.9-green.svg)](https://shields.io/)

This repository contains starter code for the IBM DevOps Capstone Project and its Python REST API microservice.

## CI/CD Tools and Practices Final Project Template

Project name: `ci-cd-final-project`

## Usage

This repository contains the sample application code, tests, and DevOps configuration. The CI workflow checks out the code, installs dependencies, runs Flake8, and executes the Nose test suite.

## Development Environment

These labs are designed to be executed in the IBM Developer Skills Network Cloud IDE with OpenShift. Please use the links provided in your Coursera lab to access the lab environment.

Initialize the environment by following the lab instructions. In the original DevOps Capstone environment, use:

```bash
source bin/setup.sh
```

This installs/configures Python 3.9 and activates the Python virtual environment.

## Useful commands

Activate the Python environment:

```bash
source ~/venv/bin/activate
```

Install dependencies:

```bash
make install
```

Start the Postgres Docker container if your lab requires it:

```bash
make db
```

## Project layout

- `service/`: Flask REST API microservice
- `tests/`: unit tests
- `requirements.txt`: Python dependencies
- `.github/workflows/workflow.yml`: CI workflow with Flake8 and Nose
- `.github/workflows/ci-build.yaml`: existing CI Build workflow
- `.tekton/tasks.yml`: cleanup and Nose Tekton tasks
- `tekton/`: existing Tekton pipeline and PVC manifests

The service uses a Model-View-Controller structure, with data and business logic in `service/models.py` and REST routes in `service/routes.py`.

## Data Model

The Account model contains these fields:

| Name | Type | Optional |
|------|------|----------|
| id | Integer | No |
| name | String(64) | No |
| email | String(64) | No |
| address | String(256) | No |
| phone_number | String(32) | Yes |
| date_joined | Date | No |

## Project task

Complete the REST APIs for READ, UPDATE, DELETE, and LIST while maintaining the expected test coverage. Follow test-driven development: write tests for the intended behavior, then implement the code to make them pass.

## Local Kubernetes Development

For local Kubernetes development outside the Cloud IDE, you may use Docker Desktop, Visual Studio Code, and the Remote Containers extension.

Example steps:

1. Create a local K3D cluster with `make cluster`.
2. Install Tekton with `make tekton`.
3. Install cluster tasks with `make clustertasks`.

## Author

[John Rofrano](https://www.coursera.org/instructor/johnrofrano), IBM Research and Coursera instructor.

## License

Licensed under the Apache License 2.0. See [LICENSE](LICENSE).

## Copyright

© IBM Corporation. All rights reserved.
