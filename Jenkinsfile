pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('Echo some text') {
      steps {
        sh 'echo "Some text"'
      }
    }
    stage('Git Checkout /Git') {
      steps {
        git(credentialsId: '2116a287-f6a4-4c2f-a5da-61c9f7dcc9ca	', url: 'https://github.com/Zolotovoloska/training-ci', branch: 'master')
      }
    }
    stage('Run app') {
      steps {
        dir(path: 'flask-app') {
          sh 'docker-compose up -d --build'
        }

      }
    }
  }
}