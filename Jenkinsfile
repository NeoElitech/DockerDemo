node {
    stage('Clone') {
        checkout scm
    }
    stage('Build') {
        docker.image('mcr.microsoft.com/dotnet/framework/sdk:4.8.1').inside {
            powershell "dotnet build -v"
        }
    }
}

// pipeline {
//     agent any
//     stages {
//         stage('Build') {
//             steps {
//                 script {
//                     docker.image('mcr.microsoft.com/dotnet/framework/sdk:4.8.1').inside {
//                     }
//                 }
//             }
//         }
//     }
//     post {
//         always{
//             cleanWs()
//         }
//     }
// }
