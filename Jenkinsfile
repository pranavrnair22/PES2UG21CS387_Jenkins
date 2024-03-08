pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                checkout([$class: 'GitSCM',
                branches: [[name: '*/main']],
                userRemoteConfigs: [[url:'https://github.com/pranavrnair22/PES2UG21CS387_Jenkins.git']]]
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
                // Introduce intentional error (nonexistent command)
                sh 'nonexistent-command'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
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
