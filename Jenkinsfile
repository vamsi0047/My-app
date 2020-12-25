pipeline {
  agent any
  stages {
    stage('hello') {
      steps {
        sh 'sh "echo helloworld"'
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