//Jenkinsfile (Declarative Pipeline)

pipeline {
    agent { label 'docker && dind-1.0.0 && 8-jdk-alpine' } { dockerfile true }
agent {
    // Equivalent to "docker build -f Dockerfile.build --build-arg version=1.0.2 ./build/
    dockerfile {
        filename 'Dockerfile'
        dir 'build'
        label 'my-defined-label'
        additionalBuildArgs  '--build-arg version=1.0.2'
        args '-v /tmp:/tmp'
    }
  }
}
