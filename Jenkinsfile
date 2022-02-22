// node {
// 	stage('Build') {
// 		echo "Build"
// 	}
// 	stage('Test') {
// 		echo "Test"
// 	}
// 	stage('Integration Test') {
// 		echo "Test"
// 	}
// }
pipeline {
	agent any
	// agent { docker { image 'maven:3.6.3' } } 
	agent { docker { image 'node:latest' } }
	stages {
		stage('Build') {
			steps {
				sh 'mvn --version'
				echo "Build"
			}
		}
		stage('Test') {
			steps {
				echo "Test"
			}
		}
		stage('Integration Test') {
			steps {
				echo "Integration Test"
			}
		}
	}
	post {
		always {
			echo 'I run always'
		}
		success {
			echo 'I run when it is successful'
		}
		failure {
			echo 'I run when it fails'
		}
	}
}