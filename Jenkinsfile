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

sh 'javac hello.java'

}

}

stage('Package') {

steps {

sh 'jar cf HelloWorld.jar hello.class'

}

}

}
