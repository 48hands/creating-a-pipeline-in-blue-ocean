pipeline {
  agent {
    docker {
      image 'node:latest'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'echo "Hello World"'
            sh 'npm --version'
            timestamps()
          }
        }
        stage('Build2') {
          steps {
            sh 'echo "Build2"'
          }
        }
      }
    }
    stage('Deliver') {
      steps {
        input 'Continue?'
        echo 'Deploy Deploy'
      }
    }
  }
}