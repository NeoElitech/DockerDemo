pipeline {
    agent any
    environment {
        WORKSPACE = pwd()
    }
    stages {
        stage('Build') {
            steps {
                script {
                    def myImage = docker.image('mcr.microsoft.com/dotnet/framework/sdk:4.8.1')
                    myImage.withRun() { c ->
                    }
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    def myImage = docker.image('mcr.microsoft.com/dotnet/framework/sdk:4.8.1')
                    myImage.withRun() { c ->
                    }
                }
            }
        }
    }
}
