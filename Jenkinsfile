pipeline {
    agent any
    stages {
        stage('Build image') {
            steps {
                sh 'docker build -t cicd-learning:${BUILD_NUMBER} .'
            }
        }
        stage('Run tests') {
            steps {
                sh 'docker run --rm cicd-learning:${BUILD_NUMBER} npx playwright test --project=chromium --reporter=list'
            }
        }
    }
}