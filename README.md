CI GitHub Actions Demo

This project demonstrates basic Continuous Integration (CI) using GitHub Actions.

Workflows

1. Python Tests

File: .github/workflows/simple-workflow.yml

Runs every time code is pushed to the main branch.

Tasks:

* Checks out the repository.
* Sets up Python.
* Upgrades pip.
* Runs the unit tests.
* Uses a matrix build to test the project with:
    * Python 3.7
    * Python 3.8
    * Python 3.9
    * Python 3.10

⸻

2. Nightly Build

File: .github/workflows/nightly-build.yml

Runs every day at midnight (UTC).

Tasks:

* Checks out the repository.
* Prints the message:

Scheduled build completed successfully!

For testing, workflow_dispatch was also added so the workflow can be started manually from the GitHub Actions page.

Files

* main.py - Contains a simple add() function.
* test_main.py - Unit tests for the add() function.
* .github/workflows/simple-workflow.yml - Python test workflow.
* .github/workflows/nightly-build.yml - Scheduled workflow.
