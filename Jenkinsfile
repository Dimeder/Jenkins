pipeline {
  agent any
  stages {
    stage('Buzz Build') {
      steps {
        sh 'echo Build > Build.txt'
        archiveArtifacts(artifacts: '*.txt', fingerprint: true)
      }
    }

    stage('Buzz Test') {
      steps {
        sh 'echo Test > Test.txt'
        junit '*.txt'
      }
    }

  }
}