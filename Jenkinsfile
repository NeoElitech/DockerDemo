node {
    try {
        def dockerImage = "sdk.4.8.1:latest"
        stage('Clone') {
        }
        stage('Build') {
            println powershell(script: """Get-ChildItem env:""", returnStdout: true)
            docker.image(dockerImage).inside {
                println powershell (script: """C:/ELITech/DevHub/Scripts/BuildSolution.ps1 -SolutionPath "Hello" """, returnStdout: true)
            }
        }
    }
    finally {
        cleanWs()
    }
}