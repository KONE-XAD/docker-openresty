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
nginx -g \'daemon off;\''''
      }
    }
  }
  environment {
    dockerv = '21'
  }
}