node {
    try {
        def dockerImage = "sdk.4.8.1:latest"
        stage('Clone') {
        }
        stage('Build') {
            docker.image(dockerImage).inside {
                powershell script: """C:/ELITech/DevHub/Scripts/BuildSolution.ps1 -SolutionPath "Hello" """
            }
        }
    }
    finally {
        cleanWs()
    }
}