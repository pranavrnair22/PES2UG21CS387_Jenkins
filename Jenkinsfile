

pipeline{
	agent any
	stages {
		stage('Clone repository') {
			steps {
				checkout ([$class: 'GitSCM',
				branches: [[name: '*/main']],
				userRemoteConfigs: [[url:'https://github.com/pranavrnair22/PES2UG21CS387_Jenkins.git']]])
			}
		}
		ngngfnfgn
		stage('Build') {
			steps {
				build 'PES2UG21CS387-1'
				sh 'g++ main.cpp -o output'
				erro_comming
			}
		}
		stage('Test') {
			steps {
				sh './output'
			}
		}	

		stage('Deploy') {
			steps {
				echo 'deploy'
			}
		}
	}
	post{
		failure{
			error 'Pipeline failed'
		}
	}
}
