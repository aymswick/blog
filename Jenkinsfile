pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'figlet "Building Blog Project"'
                sh 'echo "Checking node version..."'
                sh 'npm --version'
                sh 'npm install'
            }
        }
    }
}
