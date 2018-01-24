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
        sh "echo 'Run Static Code Analysis'"
      }
    }

    stage('Unit Test') {
      steps {
        sh "echo 'Run Unit Tests'"
      }
    }

    stage('Acceptance Tests') {
      steps {
        sh "echo 'Run Acceptance Tests'"
      }
    }
  }
}
