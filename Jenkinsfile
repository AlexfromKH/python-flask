pipeline {
  agent {
    label '$NODE_NAME'
  }
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
    parameters {
    string(name: 'NODE_NAME', defaultValue: 'sony-host', description: '')
    string(name: 'IMAGE_REPO_NAME', defaultValue: 'alexfromkh/flask-app', description: '')
    string(name: 'LATEST_BUILD_TAG', defaultValue: 'build-latest', description: '')
    string(name: 'DOCKER_COMPOSE_FILENAME', defaultValue: 'docker-compose.yml', description: '')
    booleanParam(name: 'PUSH_DOCKER_IMAGES', defaultValue: true, description: '')
   }
  stages { 
    stage('stop a docker-compose'){
      steps{
	      sh "docker-compose down"
      }
    }
    stage('rebuild an image'){
      steps{
	      sh "docker-compose build"
	    }
    }
    stage('docker-compose up'){
      steps{
	      sh "docker-compose up -d"
      }
    }
  }
}
