//Jenkinsfile (Declarative Pipeline)

pipeline {
    agent { label 'docker && dind-1.0.0' } { dockerfile true }

//     checkout scm

    stages {
        stage('Test') {
            steps {
                sh 'node --version'
                sh 'svn --version'
                sh "docker logs ${c.id}"
            }
        }
    }
}

