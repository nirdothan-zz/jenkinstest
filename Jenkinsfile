pipeline {
    agent any
  
    parameters {
        choice(
            choices: 'proj1\nproj2',
            description: '',
            name: 'REQUESTED_ACTION'
            )
    }

    
    environment { 
                AN_ACCESS_KEY = credentials('my-prefined-secret-text') 
                MYVAR="hello"
            }
    
    
    
    
    stages {
        stage('env') {
            when {
               expression { MYVAR ==~ /(hello|staging)/ }
            }
            steps {
                 sh 'printenv'
                echo AN_ACCESS_KEY_USR
               
                echo "user is ${MYVAR}"
                echo env.MYVAR
            }
        }
        stage('gradle') {
            steps {
                sh '''cd untitled; ./gradlew clean build'''
            }
        }
        stage('print1') {
        
            when {
                    expression { params.REQUESTED_ACTION == 'proj1' }
            }
            steps {
                    echo "Hello, bitwiseman!"
            }
        }
        
         stage('print2') {
        
           
            steps {
                    echo PARAM1
                    echo choice2
                    echo params.choice2
                
            }
        }
    }
  
}
