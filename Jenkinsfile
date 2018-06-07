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
       
      
        
    }

    
    environment { 
            
                MYVAR="hello,goodbye,whatsup"
            }
    
    
    
    
    stages {
        stage('env') {
            steps {
                echo "GIT_COMMIT: ${GIT_COMMIT}"
                 sh 'printenv'
               
                echo "user is ${MYVAR}"
                echo env.MYVAR
            }
        }
    }
  
}
