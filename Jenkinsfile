node {
    try {
        def imageName = "sdk.4.8.1:8"
        stage('Clone') {
            powershell "git clone https://github.com/simpleinjector/SimpleInjector.git"
        }
        stage('Build') {
            docker.image(imageName).inside {
                powershell "dotnet build ./SimpleInjector/src/SimpleInjector.sln -c Release --force"
            }
        }
        stage('Test') {
            docker.image(imageName).inside {
                powershell "dotnet test ./SimpleInjector/src/SimpleInjector.sln --logger 'trx;LogFilePrefix=ts' -f net461"
            }
        }
    }
    finally {
        
    }
}