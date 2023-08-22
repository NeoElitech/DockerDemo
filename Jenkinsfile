pipeline {
    agent none
    stages {
        stage('Build') {
            agent { dockerfile true }
            steps {
                powershell 'dotnet --version'
            }
        }
        stage('Test') {
            agent { dockerfile true }
            steps {
                powershell 'dotnet --version'
            }
        }
    }
}
