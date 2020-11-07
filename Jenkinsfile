pipeline {
  agent any
  stages {
    stage('Buzz Build') {
      steps {
        sh 'echo Build'
        archiveArtifacts(artifacts: 'target/*.jar', fingerprint: true)
      }
    }

    stage('Buzz Test') {
      steps {
        sh 'echo Test'
        junit '***/reports/**/*.'
      }
    }

  }
}