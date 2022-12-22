//scripted pipeline approach
//node {
/*		echo "Build"
		echo "Test"
		echo "Integration Test"
}*/

//Declarative Pipeline approach
pipeline {
	//agent { docker {image 'maven:3.6.3'} }
	agent { docker {image 'node:alpine3.16'}}
	stages {
		stage('Build') {
			steps {
				//sh 'mvn --version'
				sh 'node --version'
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
			echo 'Im awesome. I run always'
		}
		success {
			echo 'I run when you are successful'
		}
		failure {
			echo 'I run when you fail'
		}
		changed {
			echo 'status changed'
		}
	}
}