pipeline{
    agent any
    stages{
        stage("Restore dependencies"){
            steps{
                bat 'dotnet restore'
            } 
        }
        stage("Build Project") {
            stages{
                bat 'dotnet build --no-restore'
            }
        }
        stage("Run tests"){
            stages{
                bat 'dotnet test --no-build --verbosity normal'
            }
        }
    }
  
}