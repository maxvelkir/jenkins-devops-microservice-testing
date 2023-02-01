pipeline {
	// agent any
	agent {
		docker {
			image 'maven:3.6.3-jdk-11'
			// args '-v /root/.m2:/root/.m2'
		}
	}
	stages {
		stage('Build') {
			steps {
				sh 'mvn --version'
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
		always {
			echo 'Build complete'
		}
	}
}