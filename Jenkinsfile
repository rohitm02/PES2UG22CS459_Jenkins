pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES2UG22CS449-1'
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deployed by the king'
            }
        }
    }
    post {
        failure {
            error 'pipeline has failed father, time for reconstruction'
        }
    }
}
