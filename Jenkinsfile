pipeline {
    agent any

    tools {
        maven 'Maven' // Make sure 'Maven' is defined in Global Tool Configuration
    }

    stages {
        stage('SCM Checkout') {
            steps {
                echo 'Hello, we started the SCM-Checkout Process'
                git 'https://github.com/Prajwalatkare1/maven-project.git'
                echo 'Hello, we ended the SCM-Checkout Process'
            }
        }

        stage('Validate the Code') {
            steps {
                echo 'Hello, we started the Code Validation Process'
                withMaven(globalMavenSettingsConfig: '', jdk: '', maven: 'Maven', mavenSettingsConfig: '', traceability: true) {
                    sh 'mvn validate'
                }
                echo 'Hello, we ended the Code Validation Process'
            }
        }

        stage('Compile the Code') {
            steps {
                echo 'Hello, we started the Code Compile Process'
                withMaven(globalMavenSettingsConfig: '', jdk: '', maven: 'Maven', mavenSettingsConfig: '', traceability: true) {
                    sh 'mvn compile'
                }
                echo 'Hello, we ended the Compile Process'
            }
        }
    }
}
