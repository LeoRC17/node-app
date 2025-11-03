pipeline {
  agent {
    docker {
      image 'node:20'
    }
  }
  stages {
    stage('Install') {
      steps {
        sh 'npm install'
      }
    }
    stage('Test') {
      steps {
        sh 'npm test'
      }
    }
    stage('Run') {
      steps {
        sh 'node index.js'
      }
    }
  }
}
