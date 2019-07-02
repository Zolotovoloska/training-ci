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
  }
}