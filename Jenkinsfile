pipeline {
    agent {
        label 'java-docker-slave'
    }
    stages {
        stage('Build') {
            steps { 
                echo 'Building'
                echo 'Building2'
                def result = sh(script: 'which java', returnStatus: true)
                if (result == 0) {
                    def location = sh(script: 'which ls', returnStdout: true).trim()
                    echo "Location of 'ls' command: ${location}"
                } else {
                    error "'ls' command not found"
                }
            }
        }
        stage('Test') {
            steps { 
                echo 'Testing'
            }
        }
        stage('Deploy') {
            steps { 
                echo 'Deploying'
            }
        }
    }
}