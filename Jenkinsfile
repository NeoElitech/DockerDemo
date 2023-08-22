node {
    stage('Clone') {
        checkout scm
    }
    stage('Build') {
        def tasks = [:]
        for (int i = 0; i < 5; i++) {
            tasks["T_${i}"] = {
                docker.image('mcr.microsoft.com/dotnet/framework/sdk:4.8.1').inside("-e tid=${i}") {
                    powershell "Get-ChildItem Env:"
                }
            }
        }
        parallel tasks
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
