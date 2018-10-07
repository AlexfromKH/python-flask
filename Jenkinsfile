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
          sh "pwd"
	  dir('/tmp/'){	      
	    sh "pwd"
          }
        }
      
    }
  }
}
