pipeline {
    agent any
    stages {
        stage('Restore dependencies') {
            steps {
                bat 'dotnet restore'
            }
        }
        stage('Build project') {
            steps {
                bat 'dotnet build --configuration Release --no-restore'
            }
        }
        stage('Run tests for TestProject1') {
            steps {
                bat 'dotnet test TestProject1/TestProject1.csproj --verbosity normal'
            }
        }
        stage('Run tests for TestProject2') {
            steps {
                bat 'dotnet test TestProject2/TestProject2.csproj --verbosity normal'
            }
        }
        stage('Run tests for TestProject3') {
            steps {
                bat 'dotnet test TestProject3/TestProject3.csproj --verbosity normal'
            }
        }
    }
}