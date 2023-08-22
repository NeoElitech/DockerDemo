pipeline {
    agent none
    stages {
        stage('Build') {
            steps {
                script {
                    def myImage = docker.image('dockerdemo')
                    myImage.inside("-v ${WORKSPACE}:/workspace") {
                        powershell 'dotnet --version'
                    }
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    def myImage = docker.image('dockerdemo')
                    myImage.inside("-v ${WORKSPACE}:/workspace") {
                        powershell 'dotnet --version'
                    }
                }
            }
        }
    }
}
