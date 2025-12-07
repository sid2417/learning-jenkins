pipeline {
    agent {
        label 'AGENT-1'
    }
    parameters {
        string(name: 'AGENT1', defaultValue: 'ec2-user', description: 'Iam a agent-1 working under master')
        string(name: 'Kithu', defaultValue: 'Kerala', description: 'special person')
        
    }
    options {
        // Timeout counter starts AFTER agent is allocated
        timeout(time: 30, unit: 'MINUTES')
        disableConcurrentBuilds()
        ansiColor('xterm')
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo Hi,how r u AGENT-1'
                sh 'echo today we have deployment'
                echo "Hello ${params.AGENT1}"
                echo "Hello ${params.Kithu}"
                
            }
        }
        stage('Test') {
            steps {
                sh 'echo Hi, this is todays Test, from AGENT-1'
                //sh 'sleep 10'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo Hi, this is todays Deploy, from AGENT-1'
            }
        }
    }

    post { 
        always { 
            echo 'This message will always say Hello again!'
        }
        aborted { 
            echo 'The stage is aborted'
        }
        failure { 
            echo 'The stage is failure'
        }
        success { 
            echo 'The stage is success'
        }
    }
}