node {
    
    checkout scm

    stage('Successful exit') {
        def EXECUTION_RESULT = sh (
            script: 'python application.py 0', returnStatus: true
        )
        
        echo "Exit Code: ${EXECUTION_RESULT}"
        
        if (EXECUTION_RESULT != 0) {
            currentBuild.result = 'ABORTED'
            return
        }
    }
    
    stage('Fail exit') {
        
        def EXECUTION_RESULT = sh (
            script: 'python application.py 0', returnStatus: true
        )
        
        echo "Exit Code: ${EXECUTION_RESULT}"
        
        if (EXECUTION_RESULT != 0) {
            currentBuild.result = 'ABORTED'
            return
        }
    }

}
