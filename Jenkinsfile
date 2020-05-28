pipeline {
  agent {
    docker {
      image 'node:12.16.3-alpine3.9'
      args '-p 3000:3000'
    }
  }
  environment {
    CI = 'true'
    APP_PATH = '/home/Documents/Projects/simple-node-js-react-npm-app'
  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
    stage('Test') {
      steps {
        sh '${APP_PATH}/jenkins/script/test.sh'
      }
    }
  }
}