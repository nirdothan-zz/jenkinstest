pipeline {
  agent any
  stages {
    stage('git') {
      agent any
      steps {
        git(url: 'https://github.com/kelseyhightower/nocode.git', branch: 'master')
      }
    }
  }
  parameters {
    choice(choices: '''proj1
proj2''', description: '', name: 'REQUESTED_ACTION')
  }
}