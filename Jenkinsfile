pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    docker.image('mcr.microsoft.com/dotnet/framework/sdk:4.8.1').inside('-v D:/ELITech/Jenkins:D:/ELITech/Jenkins') {
                    }
                }
            }
        }
    }
    post {
        always{
            cleanWs()
        }
    }
}
