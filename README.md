[![CI Build](https://github.com/kaustubh1-coder/devops-capstone-project/actions/workflows/ci-build.yaml/badge.svg)](https://github.com/kaustubh1-coder/devops-capstone-project/actions)
# DevOps Capstone Template

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Python 3.9](https://img.shields.io/badge/Python-3.9-green.svg)](https://shields.io/)

## CI/CD Tools and Practices Final Project Template

Project name: `ci-cd-final-project`

This repository contains the starter code for the IBM DevOps capstone project. It contains the Python REST API microservice, tests, and CI/CD configuration.

## Development Environment

Use the IBM Skills Network Cloud IDE with OpenShift provided by the course lab. Initialize the environment using the instructions provided in the lab, then run the application and tests there.

## Project layout

- `service/`: Flask REST API microservice
- `tests/`: unit tests
- `requirements.txt`: Python dependencies
- `.github/workflows/workflow.yml`: GitHub Actions CI workflow
- `.tekton/tasks.yml`: Tekton cleanup and Nose test tasks
- `.tekton/pipeline.yml`: OpenShift/Tekton pipeline definition

## CI workflow

The workflow checks out the code, installs dependencies, runs Flake8 linting, and runs Nose unit tests on pushes and pull requests targeting `main`.

## Tekton tasks

The Tekton task file defines a workspace cleanup task and a Nose unit-testing task. The OpenShift pipeline must additionally be configured for the lab cluster's installed Git clone, Flake8, Buildah, and OpenShift client tasks.

## License

This project includes source material licensed under the Apache License 2.0. See [LICENSE](LICENSE) for details.
