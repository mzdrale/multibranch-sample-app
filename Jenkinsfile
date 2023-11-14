pipeline {
    agent any
    parameters {
        booleanParam name: 'SKIP_RUN', description: 'Skip all steps, just update pipeline info'
    }

    stages {
        stage('Update info') {
            steps {
                echo "${params.SKIP_RUN}"
            }
        }
    }
}