node {
    try {
        def dockerImage = "sdk.4.8.1:latest"
        stage('Clone') {
            powershell "git clone 'https://github.com/simpleinjector/SimpleInjector.git'"
        }
        stage('Build') {
            docker.image(dockerImage).inside {
                powershell "dotnet build './SimpleInjector/src/SimpleInjector.sln' -c Release --force"
            }
        }
        stage('Test') {
            docker.image(dockerImage).inside {
                powershell "dotnet test ./SimpleInjector/src/SimpleInjector.sln --logger 'trx;LogFilePrefix=ts'"
            }
        }
    }
    finally {
        cleanWs()
    }
}