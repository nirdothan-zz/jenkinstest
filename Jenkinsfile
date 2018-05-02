pipeline {
  agent any
  stages {
    stage('git') {
      agent any
      steps {
        git(url: 'git@github.com:nirdothan/gradle1.git', branch: 'master')
      }
    }
  }
  parameters {
    choice(choices: '''proj1
proj2''', description: '', name: 'REQUESTED_ACTION')
  }
}