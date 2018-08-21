pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh '''yarn config get registry
yarn config set registry https://registry.npm.taobao.org
yarn'''
      }
    }
    stage('Test') {
      steps {
        sh 'echo \'OK\''
      }
    }
  }
}