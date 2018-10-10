pipeline {
  agent {
    node {
      label 'sony-host'
    }

  }
  stages {
    stage('pwd current location') {
      steps {
        sh 'pwd'
      }
    }
    stage('move to app dir') {
      steps {
        dir(path: '/home/alexst/dev/python/test-dev-py') {
          sh 'pwd'
        }

      }
    }
    stage('docker test') {
      steps {
        sh 'docker ps'
      }
    }
  }
}