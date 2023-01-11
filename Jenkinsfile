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
		dockerHome = tool "myDocker"
		mavenHome = tool "myMaven"
		PATH = "dockerHome/bin:$mavenHome/bin:$PATH"
	}
    stages{
		stage ('Build') {
			steps {
				echo "Build"
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER "
				echo "BUILD_ID - $env.BUILD_ID"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "BUILD_URL - $env.BUILD_URL"

			}
		}
		stage ('Test') {
			steps {
				echo 'Tested'
			}
		}
		stage ('Integration Test'){
			steps {
				echo 'integrated tested'
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
