node {
    stage('Clone') {
        checkout scm
    }
    stage('Build') {
        docker.image('mcr.microsoft.com/dotnet/framework/sdk:4.8.1').inside {
            powershell "dotnet build ./Mach5-ASW/Sources/Framework.Time.sln -c Release --force"
        }
    }
}