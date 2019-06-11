pipeline {
  agent {
    docker {
      args '--name $dockerv'
      image 'nginx:latest'
    }

  }
  stages {
    stage('get-code') {
      steps {
        git(url: 'https://github.com/KONE-XAD/docker-openresty.git', branch: 'master', changelog: true, poll: true)
      }
    }
    stage('hello') {
      environment {
        step = 'first'
      }
      steps {
        sh '''echo hello world
echo $step
pwd
hostname'''
      }
    }
  }
  environment {
    dockerv = '21'
  }
}