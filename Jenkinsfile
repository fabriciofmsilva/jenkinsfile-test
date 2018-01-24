#!groovy
pipeline {
  agent any

  // environment {
  //   git_commit_message = ''
  //   git_commit_diff = ''
  //   git_commit_author = ''
  //   git_commit_author_name = ''
  //   git_commit_author_email = ''
  // }

  stages {
    // checkout
    stage('Checkout') {
      steps {
        deleteDir()
        checkout scm
      }
    }

    // Build
    stage('Build') {
      steps {
        bat "npm install"
      }
    }

    // Static Code Analysis
    stage('Static Code Analysis') {
      steps {
        bat "npm run lint"
      }
    }

    // Unit Tests
    stage('Unit Test') {
      steps {
        bat "npm run test"
      }
    }

    // Acceptance Tests
    stage('Acceptance Tests') {
      steps {
        bat "npm run e2e"
      }
    }

    // Deploy
    stage('Deploy') {
      steps {
        echo "Deployed"
      }
    }
  }

  post {
    always {
      echo "Always"
    }
    changed {
      echo "Changed"
    }
    success {
      echo "Success"
    }
    failure {
      echo "Failure"
    }
  }
}
