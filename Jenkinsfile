pipeline {
  agent any
  stages {
    stage('gradle') {
      steps {
        sh '''cd untitled
./gradlew clean build'''
      }
    }
    stage('print') {
      steps {
        echo $AWS_PROFILE
      }
    }
  }
  environment {
    PARAMVAR = 'test'
  }
  parameters {
    string(name: 'AWS_PROFILE', defaultValue: 'prod_us-west-2', description: 'select AWS profile')
  }
}
