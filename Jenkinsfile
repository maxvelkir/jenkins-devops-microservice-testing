pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				echo 'Building..'
			}
		}
		stage('Test') {
			steps {
				echo 'Testing..'
			}
		}
		stage('Deploy') {
			steps {
				echo 'Deploying..'
			}
		}
	} 
	post {
		success {
			echo 'Build successful'
		}
		failure {
			echo 'Build failed'
		}
	}
}