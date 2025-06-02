pipeline {
    agent any
    environment {
      DOCKERHUB_CREDENTIALS = credentials('docker-dockerhub')
    }
    stages {
       stage('Build') {
           steps {
               sh 'sudo docker build -t httpd:latest .'
           }
       }
       stage('Run') {
           steps {
               sh 'sudo docker run -d --name httpd-container -p 8082:80 httpd'
           }
       }
    }
}
