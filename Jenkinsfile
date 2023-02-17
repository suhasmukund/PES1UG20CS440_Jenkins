pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o trail_output trail.cpp'
                build job: 'PES1UG20CS440-1'
            }
        }
        stage('Test') {
            steps {
                sh './trail_output > trail.txt'
                sh 'cat trail.txt'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Successful from Jenkin Pipeline'
                echos 'error detection'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline Failed!!!'
        }
    }
}
