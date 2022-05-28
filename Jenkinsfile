// Jenkinsfile (Declarative Pipeline)
pipeline {
    agent any
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
