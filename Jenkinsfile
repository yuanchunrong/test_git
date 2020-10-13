pipeline {
  agent any
  stages {
    stage('git') {
      steps {
        dir(path: '/home/shiyanlou/Code') {
          git(url: 'git@github.com:yuanchunrong/test_git.git', branch: 'main', credentialsId: '41122bb5-36d3-4887-b7fe-cdbbebb8fe66')
        }

      }
    }

    stage('build') {
      steps {
        sh 'pip2 install -r requirements.txt'
      }
    }

    stage('run') {
      steps {
        sh 'python app.py'
      }
    }

  }
}