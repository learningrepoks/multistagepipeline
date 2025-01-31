pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'dev branch'
            }
        }
        stage('only on dev') {
             when {
                branch 'dev'
            }
            steps {
                sh """
                echo "Running Unit Tests on dev branch"
                """
            }
        }
        stage('only on nonprod') {
             when {
                branch 'nonprod'
            }
            steps {
                sh """
                echo "Running Unit Tests on non prod branch"
                """
            }
        }
    }
}
