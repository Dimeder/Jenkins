pipeline {
  agent any
  stages {
    stage('Buzz Build') {
      steps {
        sh '''



      ./jenkins/build.sh'''
        archiveArtifacts(artifacts: 'target/*.jar', fingerprint: true)
      }
    }

    stage('Buzz Test') {
      steps {
        sh 'echo Test'
      }
    }

  }
}