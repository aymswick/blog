pipeline {
    agent { docker { image 'node:6.3' } }
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
