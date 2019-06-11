pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('build-code') {
      steps {
        sh '''echo hello
while :
do
    echo 1
    sleep 2
done'''
      }
    }
  }
  environment {
    dockerv = '21'
  }
}