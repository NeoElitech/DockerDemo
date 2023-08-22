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
                    myImage.withRun('-v D:\\ELITech\\Jenkins:D:\\ELITech\\Jenkins') { c ->
                        echo "Build">Build.txt
                    }
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    def myImage = docker.image('dockerdemo')
                    myImage.withRun('-v D:\\ELITech\\Jenkins:D:\\ELITech\\Jenkins') { c ->
                        echo "TEST">TEST.txt
                    }
                }
            }
        }
    }
}
