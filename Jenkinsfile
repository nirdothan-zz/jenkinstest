pipeline {
  agent any
  stages {
    stage('gradle') {
      steps {
        sh '''cd untitled
./gradlew clean build'''
      }
    }
  }
  environment {
    PARAMVAR = 'test'
  }
}