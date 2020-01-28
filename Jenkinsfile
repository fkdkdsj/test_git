pipeline {
  agent {
    node {
      label 'dev'
    }

  }
  stages {
    stage('git') {
      steps {
        dir(path: '/home/ubuntu/jenkins_proj') {
          git 'https://github.com/fkdkdsj/test_git.git'
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