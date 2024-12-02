pipeline {
    agent any

    environment {
        DOCKER_IMAGE = 'hello-world-java:latest' // Docker image name
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'javac HelloWorld.java'
            }
        }

        stage('Package') {
            steps {
                sh 'jar cf HelloWorld.jar HelloWorld.class'
            }
        }
    }

    post {
        success {
            echo 'Build and packaging completed successfully.'
        }
        failure {
            echo 'Build or packaging failed.'
        }
    }
}
