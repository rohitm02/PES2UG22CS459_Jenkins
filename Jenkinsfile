pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES2UG22CS459-1'
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
                echo 'deployed by the father'
            }
        }
    }
    post {
        failure {
            error 'pipeline has failed father, time to reconstruct'
        }
    }
}
