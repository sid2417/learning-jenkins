pipeline {
    agent {
        label 'AGENT-1'
    }
    options {
        // Timeout counter starts AFTER agent is allocated
        timeout(time: 1, unit: 'SECONDS')
        disableConcurrentBuilds()
        ansiColor('xterm')
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo Hi, this is todays build, from AGENT-1'
                sh 'echo this is running from AGENT-1'
            }
        }
        stage('Test') {
            steps {
                sh 'echo Hi, this is todays Test, from AGENT-1'
                //sleep(10)
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo Hi, this is todays Deploy, from AGENT-1'
            }
        }
    }
}