node {
    stage('Clone') {
        checkout scm
    }
    stage('Build') {
        docker.image('mcr.microsoft.com/dotnet/framework/sdk:4.8.1').inside {
            dotnet build -h|--help
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
