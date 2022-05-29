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
                sh 'make check'
            }
        }
//         stage('Default Test') {
//             agent { 
//                 label 'jenkins-agent'
//             }
//             steps {
//                 unstash 'app' 
//                 sh 'make check'
//             }
//             post {
//                 always {
//                     junit '**/target/*.xml'
//                 }
//             }
//         }
    }
}
