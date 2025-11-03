pipeline {
    agent any

    tools {
        // This must match the name you configured in "Global Tool Configuration"
        nodejs "Node 18"
    }

    stages {
        stage('Checkout') {
            steps {
                // Pulls your repo using the Jenkins Git plugin
                checkout scm
            }
        }

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

