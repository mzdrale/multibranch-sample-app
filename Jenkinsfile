pipeline {
    agent any
    parameters {
        booleanParam name: 'SKIP_RUN', description: 'Skip all steps, just update pipeline info'
    }

    stages {
        stage('Build') {
            steps {
                sh 'echo "Building the application"'
            }
        }
        stage('Test') {
            steps {
                execute_stage('Test', params.SKIP_RUN)
                echo "Idemooo"
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying the application"'
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
