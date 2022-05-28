pipeline {
    agent none 
    stages {
        stage('Example Jenkins-agent') {
            agent { label 'jenkins-agent' }
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
            steps {
                echo 'Hello, Docker'
                sh 'java -version'
                sh 'printenv'
            }
        }
    }
}
