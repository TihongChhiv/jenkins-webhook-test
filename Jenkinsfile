pipeline {
  agent any

  stages {

    stage('Checkout') {
      steps {
        checkout scm
      }
    }

    stage('Build') {
      steps {
        echo 'Building project...'
        sh 'echo Build success > build.txt'
      }
    }

    stage('Test') {
      steps {
        echo 'Running tests...'
        sh 'echo Test passed > test.txt'
      }
    }
  }

  post {
    success {
      archiveArtifacts artifacts: '*.txt'
    }
  }
}
