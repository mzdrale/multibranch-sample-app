pipeline {
    agent any
    parameters {
        booleanParam name: 'SKIP_RUN', description: 'Skip all steps, just update pipeline info'
    }

    stages {
        stage('Build') {
            steps {
                sh 'echo "Building application"'
                // Add build steps here
            }
        }
        stage('Test') {
            when { expression { params.SKIP_RUN != true } }
            steps {
                sh 'echo "Testing application"'
                // Add test steps here
            }
            echo "Idemooo"
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying application"'
                // Add deployment steps here
            }
        }
    }
}

def execute_stage(stage_name, skip) {
    stage(stage_name) {
        if(skip) {
            echo "Skipping ${stage_name} stage"
            return
        }
        // Add steps to test the application
    }
}
