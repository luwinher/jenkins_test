pipeline {
  agent {
    node {
      label 'dev'
    }

  }
  stages {
    stage('git') {
      steps {
        dir(path: '/home/winher/test') {
          git(branch: 'main', url: 'git@github.com:luwinher/jenkins_test.git')
        }

      }
    }

    stage('build') {
      steps {
        sh 'sudo -H pip3 install -r requirements.txt'
      }
    }

    stage('run') {
      steps {
        sh 'python3 app.py'
      }
    }

  }
}