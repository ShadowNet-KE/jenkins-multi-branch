pipeline {
    agent none 
    stages {
        stage('Example Jenkins-agent') {
            agent { label 'jenkins-agent' }
            steps {
                echo 'Hello, Jenkins Agent'
                sh 'mvn --version'
            }
        }
        stage('Example Docker') {
            agent { label 'docker' }
            steps {
                echo 'Hello, Docker'
                sh 'java -version'
            }
        }
    }
}
