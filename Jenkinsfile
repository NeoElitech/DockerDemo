pipeline {
    agent none
    stages {
        stage('Build') {
            steps {
                script {
                    docker.image('mcr.microsoft.com/dotnet/framework/sdk:4.8.1').withRun('-e MyArg=MYARG') { c ->
                    }
                }
            }
        }
    }
}
