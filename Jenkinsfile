node {
    try {
        def dockerImage = "sdk.4.8.1:latest"
        stage('Clone') {
        }
        stage('Build') {
            docker.image(dockerImage).inside {
                bat 'BuildSolution.ps1 -SolutionPath "./DecoratorDemo/DecoratorDemoApp.sln"'
            }
        }
    }
    finally {
        
    }
}