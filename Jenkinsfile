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
                AN_ACCESS_KEY = credentials('slack') 
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
