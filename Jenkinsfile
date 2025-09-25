 This is my Jenkinsfile, which defines your CI/CD pipeline.

pipeline {
    agent any 

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                // Build commands go here
                // sh 'npm install' 
                // sh 'docker build -t my-app:latest .'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Test commands go here
                // sh 'npm test' 
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Deploy commands go here
                // sh 'docker push my-app:latest'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished.'
        }
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check the logs for details.'
        }
    }
}