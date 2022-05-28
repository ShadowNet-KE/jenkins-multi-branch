pipeline {
  agent any
  environment {
    EXAMPLE_KEY = credentials('example-credentials-id') // Secret value is 'sec%ret'
  }
  stages {
    stage('Example') {
      steps {
          /* CORRECT */
          bat 'echo %EXAMPLE_KEY%'
      }
    }
  }
}
