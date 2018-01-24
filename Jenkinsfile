#!groovy
pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        bat "npm install"
      }
    }

    stage('Static Code Analysis') {
      steps {
        bat "npm run lint"
      }
    }

    stage('Unit Test') {
      steps {
        bat "npm run test"
      }
    }

    stage('Acceptance Tests') {
      steps {
        bat "npm run e2e"
      }
    }
  }
}
