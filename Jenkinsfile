pipeline {
    agent any

    stages {
        stage('Checkout Main Repo') {
            steps {
                git branch: 'main', url: 'url: 'https://github.com/Aliaa-Elbishlawy/Parking-System.git'
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
