pipeline {
    agent {
        label 'AGENT-1'
    }
    parameters {
        string(name: 'KITHU', defaultValue: 'Miss SiD', description: 'Hi this is Kith, say hi to Sid')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
        
        
        
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
        stage('Params') {
            steps {
                echo "Hello ${params.KITHU}"

                echo "Biography: ${params.BIOGRAPHY}"

                echo "Toggle: ${params.TOGGLE}"

                echo "Choice: ${params.CHOICE}"

                echo "Password: ${params.PASSWORD}"
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