# Playwright CI/CD Learning

A learning project for practicing a full workflow.

## Run with Docker

Build the image:

    docker build -t cicd-learning:1 .

Run the test inside a container:

    docker run --rm cicd-learning:1 npx playwright test --project=chromium --reporter=list

## Jenkins

Jenkins reads the Jenkinsfile from main, builds the image and runs the test.