pipeline {
    agent any // Instructs Jenkins to run this pipeline on any available executor

    stages {
        stage('Build') { 
            steps {
                echo 'Step 1: Compiling application and dependencies...'
            }
        }
        
        stage('Test') { 
            steps {
                echo 'Step 2: Executing automated testing suite...'
            }
        }
        
        stage('Deploy') { 
            steps {
                echo 'Step 3: Deploying packaged artifact to server...'
            }
        }
    }
}
