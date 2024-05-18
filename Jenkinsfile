pipeline {
    agent any

    stages {
        stage('Checkout Main Repo') {
            steps {
                git branch: 'main', url: 'https://github.com/Aliaa-Elbishlawy/last_task.git', credentialsId: 'main-repo-credentials'
            }
        }
        stage('Checkout Another Repo') {
            steps {
                dir('another-repo') {
                    git branch: 'main', url: 'https://github.com/Aliaa-Elbishlawy/Parking-System.git', credentialsId: 'another-repo-credentials'
                }
            }
        }
        stage('Execute Script from Another Repo') {
            steps {
                dir('another-repo') {
                    sh 'chmod +x CloudTask.sh'
                    sh './CloudTask.sh'
                }
            }
        }
    }
}
