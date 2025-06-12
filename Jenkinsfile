pipeline {
    agent any

  

    stages {
        stage('SCM Checkout') {
            steps {
                echo 'Hello, we started the SCM-Checkout Process'
                git 'https://github.com/Prajwalatkare1/maven-project.git'
                echo 'Hello, we ended the SCM-Checkout Process'
            }
        }

        stage('test the Code') {
            steps {
                echo 'Hello, we started the Code Compile Process'
                withMaven(maven: 'Maven') {
                    sh 'mvn package '
                }
                echo 'Hello, we ended the Compile Process'
            }
        }
    }
}
