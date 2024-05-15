// #!groovy
// pipeline {
//   agent any
//   tools {
//     jdk 'jdk17'
//     maven 'maven3'
//   }
//   stages {
//     stage('Compile mavev') {
//       steps {
//         sh 'mvn compile'
//       }
//     }
//     stage('test envirnment') {
//       steps {
//         sh 'mvn test'
        
//       }
//     }
//    stage('Docker Build') {
//       agent any
//       steps {
//         sh 'docker build -t megersaj/spring-petclinic:latest .'
//       }
//     }
//     }
//   }

#!groovy

pipeline {
  agent none
  stages {
    stage('Maven Install') {
      agent {
        docker {
          image 'maven:3.5.0'
        }
      }
      steps {
        sh 'mvn clean install'
      }
    }
    stage('Docker Build') {
      agent any
      steps {
        sh 'docker build -t megersaj/spring-petclinic:latest .'
      }
    }
  }
}