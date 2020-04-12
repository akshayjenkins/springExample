pipeline {
  agent any
      tools {
        maven 'maven3'
    }
    options {
  buildDiscarder logRotator(daysToKeepStr: '5', numToKeepStr: '7')
    }
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean'
      }
    }
    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }
    stage('Deploy') {
      steps {
        sh 'mvn package'
      }
    }
  
  }
}
