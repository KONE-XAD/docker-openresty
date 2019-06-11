pipeline {
  agent {
    docker {
      image 'docker.io/nginx:latest'
      args '-P'
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