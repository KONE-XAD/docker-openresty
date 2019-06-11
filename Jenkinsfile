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
nginx'''
      }
    }
    stage('error') {
      steps {
        input(message: 'stop or wait', id: '123', ok: '465', submitter: 'stop', submitterParameter: 'wait')
      }
    }
  }
  environment {
    dockerv = '21'
  }
}