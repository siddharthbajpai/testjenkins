pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
            
                git branch: 'main', url: 'https://github.com/siddharthbajpai/testjenkins.git'
            }
        }

        stage('Checkout Branches') {
            steps {
                script {
                    
                     sh "git checkout main"
                     sh"git checkout div"
                }
            }
        }

        stage('Merge') {
            steps {
                script {
                    
                    "git merge div" 
                }
            }
        }

        stage('Push Changes') {
            steps {
                script {
                
                     sh "git push origin main"
                }
            }
        }
    }
}
