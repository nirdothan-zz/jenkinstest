pipeline {
  agent any
  stages {
    stage('git') {
      agent any
      steps {
        git(url: 'https://github.com/kelseyhightower/nocode.git', branch: 'master')
        sh '''echo "NIRNIRNIR"
ls -l
echo "my location"
pwd'''
      }
    }
    stage('env') {
      parallel {
        stage('env') {
          steps {
            sh '''ls -l
echo "my location"
pwd'''
          }
        }
        stage('parallel') {
          steps {
            echo 'parallel step'
          }
        }
      }
    }
    stage('try') {
      steps {
        echo 'dummyset'
      }
    }
  }
  parameters {
    choice(choices: '''proj1
proj2''', description: '', name: 'REQUESTED_ACTION')
  }
}