pipeline {
  agent {
    label 'sony-host'
  }
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
    parameters {
    string(name: 'WORKING_DIRECTORY', defaultValue: '/home/alexst/dev/python/test-dev-py', description: '')
    }
    stages { 
      stage('stop a docker-compose'){
        steps{
	  dir("$WORKING_DIRECTORY") {
	    sh "hostnamectl"
	    sh "pwd"
          }
        }
      }
    }
  }
}
