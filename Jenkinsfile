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

    stage('Test') {
      steps {
        sh 'cd ./example-react; npm run test -- --coverage --watchAll=false'
      }
    }

  }
}