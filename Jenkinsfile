node {
    def imageName = "sdk.4.8.1:latest"
    stage('Clone') {
        powershell "git clone https://github.com/khellang/Scrutor.git"
    }
    stage('Build') {
        docker.image(imageName).inside {
            powershell "dotnet build ./Scrutor/Scrutor.sln -c Release --force"
        }
    }
    stage('Test') {
        docker.image(imageName).inside {
            powershell "dotnet test ./Scrutor/Scrutor.sln --logger 'trx;LogFilePrefix=ts'"
        }
    }
}