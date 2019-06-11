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
        input(message: 'stop or wait', id: 'Procced', ok: 'Abort', submitter: 'Procced', submitterParameter: 'Abort')
      }
    }
  }
  environment {
    dockerv = '21'
  }
}