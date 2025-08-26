// A minimal, yet complete, example of a Jenkins Declarative Pipeline.

// The root of the pipeline
pipeline {
    // Defines where the pipeline will run. 'any' means any available agent.
    agent any

    // The stages block contains all the stages of the pipeline
    stages {
        // First stage: Build
        stage('Build') {
            steps {
                // 'sh' step executes a shell command (for Linux/macOS)
                echo "Building the application..."
            }
        }

        // Second stage: Test
        stage('Test') {
            steps {
                echo "Running unit tests..."
                // Use a different agent or tool for this stage
            }
        }

        // Third stage: Deploy
        stage('Deploy') {
            steps {
                echo "Deploying the application..."
                // Example of a conditional deployment step
            }
        }
    }

    // The post block defines actions that run after the pipeline completes
    post {
        // Runs regardless of the pipeline outcome (success or failure)
        always {
            echo 'Pipeline finished!'
        }
        // Runs only if the pipeline was successful
        success {
            echo 'Deployment was successful! 🎉'
        }
        // Runs only if the pipeline failed
        failure {
            echo 'The pipeline failed. Check the logs for details. ❌'
        }
    }
}
