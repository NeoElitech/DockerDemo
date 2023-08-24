node {
    try {
        def dockerImage = "sdk.4.8.1:latest"
        stage('Clone') {
        }
        stage('Build') {
            docker.image(dockerImage).inside {
                powershell script: "Get-ChildItem Env:*"
                powershell script: 'Get-Content -Path $env.Scripts/BuildSolution.ps1'
                powershell script: '$env.Scripts/BuildSolution.ps1 -SolutionPath ./DecoratorDemo/DecoratorDemoApp.sln'
            }
        }
    }
    finally {
        
    }
}