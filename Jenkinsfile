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
        echo "param is ${params.nir}"
      }
    }
  }
  environment {
    PARAMVAR = 'test'
  }
  parameters {
    string(name: 'nir', defaultValue: 'prod_us-west-2', description: 'select AWS profile')
  }
}
