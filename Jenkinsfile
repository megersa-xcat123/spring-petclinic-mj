#!groovy
pipeline {
  agent nany
  stages {
    stage('Maven Install') {
      steps {
        sh 'mvn clean install'
      }
    }
    stage('Docker Build') {
      steps {
        scripts{
            sh 'docker build -t shanem/spring-petclinic:latest .'
        }
        
      }
    }
  }
}