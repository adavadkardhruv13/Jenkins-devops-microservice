//scripted
/*node {
	
		echo "Build"
		echo "Test"
		echo "Integration Test"
	}*/

// Declerative

pipeline{
	agent any
    stages{
		stage ('Build') {
			steps {
				echo 'Build'
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
