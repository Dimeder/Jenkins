pipeline {
  agent {
    node {
      label 'java7'
    }

  }
  stages {
    stage('Buzz Build') {
      steps {
        sh 'echo $BUZZ_NAME > Build.txt'
        archiveArtifacts(artifacts: '*.txt', fingerprint: true)
      }
    }

    stage('Testing A') {
      parallel {
        stage('Buzz Test') {
          steps {
            sh 'echo Test > Test.txt'
            node(label: 'docker')
          }
        }

        stage('Testing B') {
          steps {
            sh '''sleep 10
echo done'''
          }
        }

        stage('Testing C') {
          steps {
            sh '''sleep 10
echo done'''
          }
        }

      }
    }

  }
  environment {
    BUZZ_NAME = ' Worker Bee'
  }
}