pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('Build') {
      steps {
        echo 'Building...'
        sh 'pwd & ls'
      }
    }
    stage('Test') {
      steps {
        echo 'Testing...'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying...'
      }
    }
  }
}