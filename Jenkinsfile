pipeline {
    agent any

    stages {
        stage('SCM Checkout') {
            steps {
                echo 'Hello, we started the SCM-Checkout Process'
                git 'https://github.com/Prajwalatkare1/maven-project.git'
                echo 'Hello, we ended the SCM_Checkout Process'
            }
        }
      stage('Validate the Code') {
            steps {
                echo 'Hello, we started the SCM-Checkout Process'
                git 'https://github.com/Prajwalatkare1/maven-project.git'
                echo 'Hello, we ended the SCM_Checkout Process'
            }
      }

       stage('SCM Checkout') {
            steps {
                echo 'Hello, we started the SCM-Checkout Process'
              withMaven(globalMavenSettingsConfig: '', jdk: '', maven: 'Maven', mavenSettingsConfig: '', traceability: true) {
            //some block
              }
                echo 'Hello, we ended the SCM_Checkout Process'
            }
       }



    }
}
