//scripted
/*node {
	
		echo "Build"
		echo "Test"
		echo "Integration Test"
	}*/

// Declerative

pipeline{
	agent any
	//agent {docker {image 'maven:3.8.7'}}
	environment {
		//dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven' 
		// "$dockerHome/bin:
		PATH = "$mavenHome/bin:$PATH"
	}
    stages{
		stage ('Checkout') {
			steps {
				sh 'mvn --version'
				//sh 'docker version'
				echo "Build"
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER "
				echo "BUILD_ID - $env.BUILD_ID"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "BUILD_URL - $env.BUILD_URL"

			}
		}
		stage("Complie") {
			steps {
				sh "mvn clean complie"
			}
		}
		stage ('Test') {
			steps {
				sh 'mvn test'
			}
		}
		stage ('Integration Test'){
			steps {
				sh 'mvn failsafe:integration-test failsafe:verify'
			}
		}
	}
	post {
		always {
			echo 'Im awesome, I run always'
		}
		success {
			echo 'I run when you are successful '
		}
		failure {
			echo'I run when you fail'
		}
	}
}
