node {
    stage('Clone') {
        git(url: 'https://github.com/ELITechgroup-CS/Mach5-ASW.git', branch: 'main', credentialsId: 'NeoElitech')
    }
    stage('Build') {
        docker.image('mcr.microsoft.com/dotnet/framework/sdk:4.8.1').inside {
            powershell "dotnet test -h"
        }
    }
}