node {
    try {
        def dockerImage = "sdk.4.8.1:latest"
        stage('Clone') {
            println powershell(script: "git clone https://github.com/NeoElitech/DecoratorDemo.git", returnStdout: true)
        }
        stage('Build') {
            println powershell(script: """Get-ChildItem env:""", returnStdout: true)
            docker.image(dockerImage).inside {
                println powershell(script: """C:/ELITech/DevHub/Scripts/BuildSolution.ps1 -SolutionPath "./DecoratorDemoApp/DecoratorDemoApp.sln" """, returnStdout: true)
            }
        }
    }
    finally {
        cleanWs()
    }
}