pipeline {
    agent any
    parameters {
        string(defaultValue: 'master', description: '', name: 'gitBranch')
    }


    
    stages {
        stage('env') {
            steps {
               script{
                   MYTAG=sh(script: '''
                   #!/bin/bash
                   tag=`git describe --exact-match --tags ${GIT_COMMIT} 2> /dev/null` || status=$?
                   if [ $status -eq 0 ]
                   then
                      echo $tag
                   else
                      echo 0
                   fi
                   ''', returnStdout: true).trim()
               }
               echo "MYTAG=${MYTAG}" 
            }
        }
    }
  
}
