pipeline {
  agent {
    docker {
      image 'docker.io/nginx:latest'
    }

  }
  stages {
    stage('build-code') {
      steps {
        sh '''hostname
pwd
cat /etc/hosts
curl 127.0.0.1'''
      }
    }
  }
  environment {
    dockerv = '21'
  }
}