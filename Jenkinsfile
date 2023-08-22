node {
    stage('Clone') {
        checkout scm
    }
    stage('Build') {
        def tasks = [:]
        for (int i = 0; i < 20; i++) {
            tasks["T_${i}"] = {
                docker.image('mcr.microsoft.com/dotnet/framework/sdk:4.8.1').inside {
                    powershell "ECHO Hello_From_T"
                }
            }
            parallel tasks
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
