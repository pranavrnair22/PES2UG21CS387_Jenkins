pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                checkout([$class: 'GitSCM',
                branches: [[name: '*/main']],
                userRemoteConfigs: [[url:'https://github.com/pranavrnair22/PES2UG21CS387_Jenkins.git']]])
            }
        }
        stage('Build') {
            steps {
                build 'PES2UG21CS387-1'
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                SH './output
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
            // Additional actions or notifications can be added here
        }
    }
}
