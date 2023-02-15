pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o cs455_output cs455.cpp'
                build job: 'PES1UG20CS455-1'
            }
        }
        stage('Test') {
            steps {
                sh './cs455_output > cs455.txt'
                sh 'cat cs455.txt'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Successful by Jenkins'
                echos 'Hello World'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline Failed!'
        }
    }
}
