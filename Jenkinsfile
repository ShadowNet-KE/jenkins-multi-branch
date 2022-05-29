// Jenkinsfile (Declarative Pipeline)
pipeline {
    agent { label 'docker && dind-1.0.0 && 8-jdk-alpine && jenkins-agent' }
    options {
      buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '2', numToKeepStr: '20')
    }
    stages {
        stage('Build') { 
            steps {
                sh 'ls'
            }
        }
        stage('Test') { 
            steps {
                sh 'df -h'
            }
        }
        stage('Deploy') { 
            steps {
                sh 'ls -lh'
            }
        }
    }
}
