pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo "${BRANCH_NAME}"
            }
        }
        stage('only on dev') {
             when {
                branch 'dev'
            }
            steps {
                sh """
                echo "${BRANCH_NAME}"
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
         stage('only on prod') {
             when {
                branch 'prod'
            }
            steps {
                sh """
                echo "Running Unit Tests on non prod branch"
                """
            }
        }
    }
}
