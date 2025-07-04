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

        stage('Deploy  the tom cat server') {
            steps {
              sshagent(['DEVCICD']) {
                	sh 'scp -o StrictHostKeyChecking=no webapp/target/webapp.war ec2-user@16.16.186.222:/usr/share/tomcat/webapps'
    
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
