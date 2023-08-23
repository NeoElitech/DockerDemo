node {
    stage('Clone') {
        checkout scm
    }
    stage('Build') {
        docker.image('mcr.microsoft.com/dotnet/framework/sdk:4.8.1').inside {
            powershell "dotnet build ./Mach5-ASW/Sources/Framework.Time.sln -c Release --force"
        }
    }
    stage('Test') {
        docker.image('mcr.microsoft.com/dotnet/framework/sdk:4.8.1').inside {
            powershell "dotnet test ./Mach5-ASW/Sources/_test/Framework.Time/Release/ELITech.Tests.Framework.Time.dll --logger 'trx;logfilename=testResults.trx'"
        }
    }
}