pipeline {
    agent any

    stages {
        stage('Stage 1') {
            steps {
                echo "This is Stage 1"
                 sh 'dotnet clean'
                 sh 'dotnet restore'

                // Build the .NET Core project
                sh 'dotnet build'
            }
        }

        stage('Stage 2') {
            steps {
                echo "This is Stage 2"
                // Add your commands or build steps here for Stage 2
            }
        }

        stage('Stage 3') {
            steps {
                echo "This is Stage 3"
                // Add your commands or build steps here for Stage 3
            }
        }
    }

    post {
        always {
            echo "Pipeline completed"
        }
    }
}
