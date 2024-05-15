#!groovy
pipeline {
  agent any
  tools {
    jdk 'jdk17'
    maven 'maven3'
  }
  stages {
    stage('Compile mavev') {
      steps {
        sh 'mvn test'
      }
    }
    stage('test envirnment') {
      steps {
        sh 'mvn test'
        
      }
    }
  }
}