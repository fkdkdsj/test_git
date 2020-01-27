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
          git(url: 'https://github.com/fkdkdsj/test_git/tree/master', credentialsId: 'dd0cb059-cb7e-410e-8290-1b2b30b68f3d')
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