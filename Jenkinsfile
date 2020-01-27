pipeline {
  agent {
    node {
      label 'self-node'
    }

  }
  stages {
    stage('git') {
      steps {
        dir(path: '/home/ubuntu/git_jenkins') {
          git 'https://github.com/fkdkdsj/test_git/tree/master'
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