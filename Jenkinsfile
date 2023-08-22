pipeline {
    agent any
    environment {
        WORKSPACE = pwd()
    }
    stages {
        stage('Build') {
            steps {
                script {
                    def myImage = docker.image('dockerdemo')
                    myImage.inside("-v ${env.WORKSPACE}:\\workspace") {
                        powershell 'dotnet --version'
                    }
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    def myImage = docker.image('dockerdemo')
                    myImage.inside("-v ${env.WORKSPACE}:\\workspace") {
                        powershell 'dotnet --version'
                    }
                }
            }
        }
    }
}
