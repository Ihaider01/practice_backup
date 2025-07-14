pipeline {
    agent {
        docker {
            image 'node:18'
            args '-v ${WORKSPACE}:/workspace -w /workspace'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'node -v'
                sh 'echo "Running build step..."'
            }
        }
    }
}
