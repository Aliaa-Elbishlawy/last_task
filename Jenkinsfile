pipeline {
    agent any
    
    stages {
        stage('Checkout Main Repo') {
            steps {
                git branch: 'main', url: 'https://github.com/Aliaa-Elbishlawy/last_task.git'
            }
        }
        stage('Execute Script in Main Repo') {
            steps {
                sh 'chmod +x CloudTask.sh'
                sh './CloudTask.sh'
            }
        }
        stage('Checkout Another Repo') {
            steps {
                // Checkout the second repository
                git branch: 'main', url: 'https://github.com/Aliaa-Elbishlawy/Parking-System.git'
            }
        }
        stage('Execute Script in Another Repo') {
            steps {
                // Ensure the script is executable and run it in the second repository
                sh 'chmod +x another_repo.sh'
                sh './another_repo.sh'
            }
        }
    }
}
