// Jenkinsfile (Scripted Pipeline)

node {
    /* Requires the Docker Pipeline plugin to be installed */
    docker.image('node:16.13.1-alpine').inside {
        stage('Test') {
            sh 'node --version'
        }
    }
}

