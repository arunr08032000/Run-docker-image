pipeline {
    agent any
    environment {
      DOCKERHUB_CREDENTIALS = credentials('docker-dockerhub')
    }
    stages {
       stage('Build') {
           steps {
               sh 'sudo docker build -t alpine:3.13.5 .'
           }
       }
       stage('Test') {
           steps {
               sh 'sudo docker run --name test alpine:3.13.5'
           }
       }
    }
}
