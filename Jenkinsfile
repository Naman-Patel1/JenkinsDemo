pipeline {

    agent any

    tools {
        jdk 'JDK25'
        maven 'Maven'
    }

    stages {

        stage('Build') {
            steps {
                bat 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
    }

    post {

        success {
            echo 'BUILD AND TEST SUCCESSFUL'
        }

        failure {
            echo 'BUILD OR TEST FAILED'
        }
    }
}