pipeline {
    agent any
    stages {
        stage('DEMO STAGE') {
            steps {
                script {
                    sh 'echo "My DEMO PIPELINE is working fine."'
                    sh 'echo "Creating a file to test..."'
                    sh 'touch ./pipeline_build_working_demo'
                    sh 'echo "Successfully created"'
                }
            }
        }
    }
} 
