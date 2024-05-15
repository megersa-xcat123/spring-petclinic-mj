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
        sh 'mvn compile'
      }
    }
    stage('test envirnment') {
      steps {
        sh 'mvn test'
        
      }
    }
    tage('Build Docker') {
      steps {
        scripts{
            sh 'docker build -t megersaj/spring-petclinic:latest .'

        }
        
      }
    }
  }
}

