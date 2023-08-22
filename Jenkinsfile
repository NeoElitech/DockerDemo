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
                    myImage.inside() {
                        echo "Build">Build.txt
                    }
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    def myImage = docker.image('dockerdemo')
                    myImage.inside() {
                        echo "TEST">TEST.txt
                    }
                }
            }
        }
    }
}
