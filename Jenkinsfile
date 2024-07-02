pipeline {
    agent any
    
    stages {
        stage('Copy File') {
            steps {
                script {
                
                    def sourceDir = '/Users/paras/Documents/siddpython'
                    def destDir = '/Users/paras/Documents/siddharth1'
                    
                    
                    def fileName = 'main.py'
                    
                    
                    sh "cp ${sourceDir}/${fileName} ${destDir}/${fileName}"
                    
                    
                  
                }
            }
        }
    }
}
