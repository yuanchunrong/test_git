pipeline {
  agent any
  stages {
    stage('git') {
      steps {
        dir(path: '/home/shiyanlou/Code') {
          git(url: 'git@github.com:yuanchunrong/test_git.git', branch: 'main', credentialsId: '733ce676-5e9e-4172-b321-011d9dacb803')
        }

      }
    }

    stage('build') {
      steps {
        sh 'pip install -r requirements.txt'
      }
    }

    stage('run') {
      steps {
        sh 'python app.py'
      }
    }

  }
}