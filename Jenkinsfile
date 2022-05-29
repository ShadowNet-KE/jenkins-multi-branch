pipeline {
    agent none
    options {
      buildDiscarder logRotator(artifactDaysToKeepStr: '5', artifactNumToKeepStr: '10', daysToKeepStr: '5', numToKeepStr: '10')
    }
    stages {
        stage('DIND Test') {
            agent {
                label 'dind-1.0.0'
            }
            steps {
                checkout scm
                sh 'make'
            }
        }
        stage('Jenkins Test') {
            agent {
                label 'jenkins-agent'
            }
            steps {
                checkout scm
                sh 'make'
            }
        }
    }
}
