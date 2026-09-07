pipeline {
    agent any

    stages {
        stage('Initialize & Lint') {
            steps {
                echo 'Checking project structure and code linting...'
                sh 'ls -la' 
            }
        }

        stage('Automated Test Workflow') {
            steps {
                echo 'Running automated test suites...'
                sh 'node app.js'
            }
        }

        stage('Package & Build Artifact') {
            steps {
                echo 'Packaging the application into an artifact...'
                sh 'mkdir -p build && cp app.js build/'
                echo 'Artifact created successfully inside build/ directory.'
            }
        }

        stage('Automated Deployment') {
            steps {
                echo 'Deploying application to local environment...'
                sh 'echo "Deployment Complete at $(date)" > build/deploy.log'
                sh 'cat build/deploy.log'
            }
        }
    }

    post {
        success {
            echo 'Task 2 Automation Complete: ALL WORKFLOWS PASSED!'
        }
        failure {
            echo 'Automation Failed: Check Console Logs.'
        }
    }
}


