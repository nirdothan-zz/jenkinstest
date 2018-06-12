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
                   tag=`git describe --tags ${GIT_COMMIT}`
                   if [ $? -eq 0 ]
                   then
                      echo $tag
                   else
                      echo 0
                   fi
                   ''', returnStdout: true)?.trim()
               }
               echo "MYTAG=${MYTAG}" 
            }
        }
    }
  
}
