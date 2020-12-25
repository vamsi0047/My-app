pipeline {
  agent any
  stages {
    stage('hello') {
      steps {
        sh 'sh "echo hello world"'
        sh 'sh "echo step2"'
      }
    }

    stage('sleep') {
      steps {
        sleep 14
      }
    }

  }
}