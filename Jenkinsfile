pipeline {
    agent none
    options { parallelsAlwaysFailFast() }
    stages {
        stage('Example Jenkins-agent') {
            agent { label 'jenkins-agent' }
            options {
                timeout(time: 1, unit: 'HOURS') 
            }
            environment { 
                AN_ACCESS_KEY = credentials('69bd57cc-eb83-4320-aa0b-c475ebb96cf5') 
            }
            steps {
                echo 'Hello, Jenkins Agent'
                sh 'java -version'
                sh 'printenv'
            }
        }
        stage('Example Docker') {
            agent { label 'docker' }
            options {
                timeout(time: 1, unit: 'HOURS') 
            }
            steps {
                echo 'Hello, Docker'
                sh 'java -version'
                sh 'printenv'
            }
        }
    }
}
