node {
    stage('Clone') {
        checkout scm
    }
    stage('Build') {
        docker.image('mcr.microsoft.com/dotnet/framework/sdk:4.8.1').inside {
            powershell "dotnet build 'C:\\ProgramData\\Jenkins\\.jenkins\\workspace\\DockerDemo\\Mach5-ASW\\Sources\\ASW-MACH5.sln'"
        }
    }
}