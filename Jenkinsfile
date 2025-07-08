pipeline {
    agent any  // Run on any available Jenkins agent

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                // Add your build command here, e.g., mvn clean package
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add your test command here, e.g., mvn test or pytest
            }
        }

        stage('Deploy') {
            steps {
            
                sshagent(['DEVCICD']) {
         kngoindo
}           
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}