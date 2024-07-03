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
                    sh "git checkout div"
                }
            }
        }

        stage('Pull Changes from div') {
            steps {
                script {
                    
                    sh "git pull origin main"
        
                }
            }
        }

        stage('Merge') {
            steps {
                script {
                    sh "git merge div"
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
