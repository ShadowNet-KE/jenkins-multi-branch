pipeline {
    agent none
    options {
      buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '2', numToKeepStr: '20')
    }
    stages {
        stage('Build') {
            agent any
            steps {
                checkout scm
                sh 'make'
                stash includes: '**/target/*.jar', name: 'app' 
            }
        }
        stage('DIND Test') {
            agent {
                label 'dind-1.0.0'
            }
            steps {
                unstash 'app'
                bat 'make check' 
            }
            post {
                always {
                    junit '**/target/*.xml'
                }
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
