pipeline {
    agent any
    stages {
        stage('Restore') {
            steps {
                sh 'dotnet restore'
            }
        }
        stage('Clean') {
            steps {
                sh 'dotnet clean'
            }
        }
        stage('Build') {
            steps {
               sh 'dotnet build -c Release --no-restore'    
            }
        }
        stage('Publish') {
            steps {
               sh 'dotnet publish -c Release --no-build'    
            }
        }
    }
}
