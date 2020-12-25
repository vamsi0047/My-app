pipeline {
  agent any
  stages {
    stage('hello') {
      steps {
        sh 'echo helloworld'
        sh 'echo step2'
      }
    }

    stage('sleep') {
      steps {
        sleep 14
      }
    }

  }
}