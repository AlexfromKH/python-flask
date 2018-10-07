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
	  dir("/tmp"){	      
	    sh "pwd"
	    sh "hostnamectl"
	    sh "touch test"
          }
        }
      
    }
  }
}
