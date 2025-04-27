pipeline {
    agent any
    environment {
      DOCKERHUB_CREDENTIALS = credentials('docker-dockerhub')
    }
    stages {
       stage('Build') {
           steps {
               sh 'sudo docker build -t alpine:latest'
           }
       }
       stage('Test') {
           steps {
               sh 'sudo docker run -it --name test alpine:latest'
           }
       }
    }
