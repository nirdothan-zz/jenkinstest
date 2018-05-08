pipeline {
  agent any
  stages {
    stage('git') {
      agent any
      environment {
        myvar = 'nir'
      }
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
            sh 'pwd'
          }
        }
      }
    }
    stage('try') {
      steps {
        echo 'dummyset ${myvar}'
      }
    }
    stage('') {
      steps {
        readFile 'Jenkinsfile'
      }
    }
  }
  parameters {
    choice(choices: '''proj1
proj2''', description: '', name: 'REQUESTED_ACTION')
  }
}