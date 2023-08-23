node {
    stage('Clone') {
        
    }
    stage('Build') {
        docker.image('mcr.microsoft.com/dotnet/framework/sdk:4.8.1').inside {
            powershell "dotnet test -h"
        }
    }
}