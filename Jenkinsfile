pipeline {
  agent any
  stages {
    stage('gradle') {
      steps {
        sh './gradew clean build'
      }
    }
  }
  environment {
    PARAMVAR = 'test'
  }
}