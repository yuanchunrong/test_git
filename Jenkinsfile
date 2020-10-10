pipeline {
  agent any
  stages {
    stage('git') {
      steps {
        dir(path: '/home/shiyanlou/test_git') {
          git(url: 'git@github.com:yuanchunrong/test_git.git', credentialsId: '4ffdd71a-b279-4c10-9690-a81248984946', branch: 'main')
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