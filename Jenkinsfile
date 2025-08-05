pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        echo 'Installing dependencies...'
        sh 'npm install'
      }
    }

    stage('Test') {
      steps {
        echo 'Running tests (skipped for now)...'
        // If no tests, skip or use: sh 'echo No tests'
        sh 'echo No tests'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying (placeholder)...'
        // You can replace this with Docker or other deployment
        sh 'echo Deploy step complete'
      }
    }
  }
}
