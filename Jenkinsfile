pipeline {
    agent none
    stages {
        stage('Test') {
            agent {
                docker { dockerfile true }
            }
            steps {
                powershell 'dotnet --version'
            }
        }
    }
}
