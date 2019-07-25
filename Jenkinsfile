pipeline {
  agent any
  stages {
    stage('test') {
      parallel {
        stage('test') {
          steps {
            sh 'echo hello'
          }
        }
        stage('sub git') {
          steps {
            git(changelog: true, url: 'git@gitlab.inrice.top:marketing/career-talent-server.git', branch: 'nhnsh_keji')
          }
        }
      }
    }
  }
}