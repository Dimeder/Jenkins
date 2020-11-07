pipeline {
  agent any
  stages {
    stage('Buzz Build') {
      steps {
        sh 'echo $BUZZ_NAME > Build.txt'
        archiveArtifacts(artifacts: '*.txt', fingerprint: true)
      }
    }

    stage('Buzz Test') {
      steps {
        sh 'echo Test > Test.txt'
      }
    }

  }
  environment {
    BUZZ_NAME = ' Worker Bee'
  }
}