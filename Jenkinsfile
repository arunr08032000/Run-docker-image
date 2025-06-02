pipeline {
    agent any
    environment {
      DOCKERHUB_CREDENTIALS = credentials('docker-dockerhub')
    }
    stages {
       stage('Build') {
           steps {
               sh 'sudo docker build -t nginx:latest .'
           }
       }
       stage('Test') {
           steps {
               sh 'docker run -d --name nginx-container -P nginx'
           }
       }
    }
}
