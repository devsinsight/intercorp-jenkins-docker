pipeline {
  agent {
    docker {
      image 'node:latest'
      args '--network docker-jenkins_jenkinsnet'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }

  }
}