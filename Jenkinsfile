pipeline {
  agent any
  stages {
    stage('git') {
      steps {
        dir(path: '/home/shiyanlou') {
          git(credentialsId: 'c4be555e-d173-4c8e-a9a1-ac2ee50817d5', url: 'git@github.com:yuanchunrong/test_git.git', branch: 'main')
        }

      }
    }

    stage('build') {
      steps {
        sh 'sudo -H pip install -r requirements.txt'
      }
    }

    stage('run') {
      steps {
        sh 'python app.py'
      }
    }

  }
}