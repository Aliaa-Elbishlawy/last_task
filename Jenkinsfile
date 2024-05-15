pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Aliaa-Elbishlawy/last_task.git'
            }
        }
        stage('Execute Script') {
            steps {
                // Ensure the script is executable and run it
                sh 'chmod +x list_files.sh'
                sh './list_files.sh'
            }
        }
    }
}
