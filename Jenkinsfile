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
			step {
				echo 'Tested'
			}
		}
		stage ('Integration Test'){
			step {
				echo 'integrated tested'
			}
		}
	}
}
