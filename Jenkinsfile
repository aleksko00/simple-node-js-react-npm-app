pipeline {
     agent {
        docker {
            image 'node:20.15.0' // Use a Docker image with Node.js installed
            args '-u root:root' // Optional: Run as root to avoid permission issues
        }
    }
    environment {
        NODE_ENV = 'development'
    }

    stages {
        stage('Install Dependencies') {
            steps {
                // Install dependencies
                sh 'npm install'
            }
        }
    }

    post {
        always {
            // Clean workspace after build
            cleanWs()
        }
    }
}
