pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('Build') {
      steps {
        echo 'Docker logging in...'
        sh '''docker login --username=dongxuny --password=donghun221
'''
        echo 'Build docker image...'
        sh '''docker image build -t dongxuny/hellotencent . 
'''
        echo 'Tagging docker image ....'
        sh '''docker images -q | head -1 | xargs -I {} docker tag dongxuny/hellotencent dongxuny/hellotencent:{}
'''
        echo 'Pushing to dockerhub...'
        sh '''docker push dongxuny/hellotencent
'''
      }
    }
  }
}