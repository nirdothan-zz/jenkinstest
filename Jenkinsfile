pipeline {
  agent any
  stages {
    stage('gradle') {
      steps {
        sh './gradlew clean build'
      }
    }
  }
  environment {
    PARAMVAR = 'test'
  }
}