pipeline {
  agent {
    node {
      label 'dev'
    }

  }
  stages {
    stage('git') {
      steps {
        dir(path: '/home/winher/test_git') {
          git(url: 'git@github.com:luwinher/jenkins_test.git', branch: 'main')
        }

      }
    }

    stage('build') {
      steps {
        sh 'pip3 install -r requirements.txt'
      }
    }

    stage('run') {
      steps {
        sh 'python3 app.py'
      }
    }

  }
}