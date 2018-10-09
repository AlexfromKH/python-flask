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
        sh 'pwd'
	      sh 'whoami'
	      sh 'docker -v'
	      sh 'docker ps'
//        dir('/home/alexst/dev/python/test-dev-py'){	      
//	      sh 'pwd'
//        }
      } 
    }
    stage('rebuild docker-compose'){
      steps{
        sh 'pwd'
        dir('/home/alexst/dev/python/test-dev-py'){	      
	        sh 'pwd'
        }
      }  
    }  
  }
}
