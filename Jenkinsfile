pipeline {
  agent {
    label 'sony-host'
  }
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }

    stages { 
      stage('stop a docker-compose'){
        steps{
            dir ('/home/alexst/dev/python/test-dev-py}') {
	      sh "hostnamectl"
	      sh "pwd"
            }
        }
      
    }
  }
}
