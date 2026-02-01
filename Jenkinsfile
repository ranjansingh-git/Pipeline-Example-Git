pipeline {
    agent any

    environment {
        VERSION_NAME = '1.3.5'
    }
    stages {

        stage('compile') {
            steps {
            bat 'javac Test.java'
            'echo "${VERSION_NAME}"'
            }
        }

        stage('run') {
            steps {
            bat 'java Test'
            }
        }
    }

    post {

        always {
            bat 'echo always'
        }

        success {
            bat 'echo success'
        }

        failure {
            bat 'echo failure'
        }
    }
}