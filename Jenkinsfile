//Jenkinsfile (Declarative Pipeline)

pipeline {
    agent { label 'docker' } { dockerfile true }

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

