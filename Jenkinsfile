pipeline {
  agent any
  stages {
    stage('git') {
      steps {
        dir(path: '/home/winher/test') {
          git(url: 'git@github.com:luwinher/jenkins_test.git', branch: 'master')
        }

      }
    }

    stage('build') {
      steps {
        sh 'sudo -H  pip3 install -r requirements.txt'
      }
    }

    stage('run') {
      steps {
        sh 'python3 app.py'
      }
    }

  }
}