pipeline {
  agent any
  
  parameters {
          string ( name: 'AWS_PROFILE', defaultValue: 'prod_us-west-2', description: 'select AWS profile')
    }


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
