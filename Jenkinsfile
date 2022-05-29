pipeline {
    agent none
//     agent { label 'docker && dind-1.0.0 && 8-jdk-alpine' }
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
        stage('8-jdk-alpine Test') {
            agent {
                label '8-jdk-alpine'
            }
            steps {
                checkout scm
                sh 'make'
            }
        }
//         stage('Jenkins Test') { // make: not found
//             agent {
//                 label 'jenkins-agent'
//             }
//             steps {
//                 checkout scm
//                 sh 'make'
//             }
//         }
    }
}
