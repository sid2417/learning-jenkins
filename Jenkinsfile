pipeline {
    agent any
    options {
        // Timeout counter starts AFTER agent is allocated
        timeout(time: 1, unit: 'SECONDS')
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo this is new build'
            }
        }
        stage('Test') {
            steps {
                sh 'echo this is new test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo this is new deploy'
            }
        }
    }
}