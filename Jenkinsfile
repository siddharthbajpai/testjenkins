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

        stage('Pull Changes') {
            steps {
                script {
                    
                    sh "git pull origin main"
                    sh "git pull origin div"
                    sh "  git config pull.rebase false  # merge"
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
