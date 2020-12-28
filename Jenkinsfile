pipeline {
  agent any
  stages {
    stage('hello') {
      parallel {
        stage('hello') {
          steps {
            sh 'echo helloworld'
            sh 'echo step2'
          }
        }

        stage('') {
          steps {
            sh 'echo running in parllel'
          }
        }

      }
    }

    stage('sleep') {
      steps {
        sleep 14
      }
    }

  }
}