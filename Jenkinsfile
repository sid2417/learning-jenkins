pipeline {
    agent {
        label 'AGENT-1'
    }
    // options {
    //     // Timeout counter starts AFTER agent is allocated
    //     timeout(time: 15, unit: 'SECONDS')
    //     disableConcurrentBuilds()
    // }
    stages {
        stage('Build') {
            steps {
                sh 'echo this is new build'
                sh 'THis is running from AGENT-1'
            }
        }
        stage('Test') {
            steps {
                sh 'echo this is new test'
                sleep(10)
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo this is new deploy'
            }
        }
    }
}