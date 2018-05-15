pipeline {
    agent any
  
    parameters {
        choice(
            choices: 'proj1\nproj2',
            description: '',
            name: 'REQUESTED_ACTION'
            )
        string(defaultValue: 'master', description: '', name: 'gitBranch')
        booleanParam(defaultValue: true, description: '', name: 'userFlag1')
        booleanParam(defaultValue: true, description: '', name: 'userFlag2')
        booleanParam(defaultValue: true, description: '', name: 'userFlag3')
        booleanParam(defaultValue: true, description: '', name: 'userFlag4')
        booleanParam(defaultValue: true, description: '', name: 'userFlag5')
        booleanParam(defaultValue: true, description: '', name: 'userFlag6')
        booleanParam(defaultValue: true, description: '', name: 'userFlag7')
        booleanParam(defaultValue: true, description: '', name: 'userFlag8')
        booleanParam(defaultValue: true, description: '', name: 'userFlag9')
        booleanParam(defaultValue: true, description: '', name: 'userFlag10')
        booleanParam(defaultValue: true, description: '', name: 'userFlag11')
        booleanParam(defaultValue: true, description: '', name: 'userFlag12')
        booleanParam(defaultValue: true, description: '', name: 'userFlag13')
        booleanParam(defaultValue: true, description: '', name: 'userFlag14')
        booleanParam(defaultValue: true, description: '', name: 'userFlag15')
        booleanParam(defaultValue: true, description: '', name: 'userFlag16')
        booleanParam(defaultValue: true, description: '', name: 'userFlag17')
        booleanParam(defaultValue: true, description: '', name: 'userFlag18')
      
        
    }

    
    environment { 
                AN_ACCESS_KEY = credentials('my-prefined-secret-text') 
                MYVAR="hello,goodbye,whatsup"
            }
    
    
    
    
    stages {
        stage('env') {
            when {
               expression { MYVAR ==~ /(.*)goodbye,,(.*)/ }
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
