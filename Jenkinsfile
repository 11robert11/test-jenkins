pipeline {
  agent none
  }
  stages {

    stage('Build') {
      agent {
        docker {
          image 'maven:3.8.7-eclipse-temurin-11'
          args '-v /root/.m2:/root/.m2 --dns	127.0.0.1 --net=host'
        }
      steps {
        sh 'mvn -B clean package'
      }

    }

    stage('Deliver') {
    agent any
      steps {
        sh 'ls'
      }
    }

  }
}