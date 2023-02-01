pipeline {
	agent any
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	// agent {
	// 	docker {
	// 		image 'maven:3.6.3-jdk-11'
	// 	}
	// }
	stages {
		stage('Build') {
			steps {
				echo 'Building..'
				sh 'mvn --version'
				sh 'docker --version'
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