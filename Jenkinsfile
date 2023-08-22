pipeline {
    agent none
    stages {
        stage('Test') {
            agent { dockerfile true }
            steps {
                powershell 'dotnet --version'
            }
        }
    }
}
