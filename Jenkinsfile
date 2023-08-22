pipeline {
    agent none
    stages {
        stage('Build') {
            steps {
                script {
                    docker.image('mysql:8-oracle').withRun() { c->
                    }
                }
            }
        }
    }
}
