// Scripted
// node {
// 	echo "Build"
// 	echo "Test"
// 	echo "Integration Test"
// }

// Declarative

pipeline {
	agent any
	stages{
		stage('Build'){
			steps {
				echo "Build"	
			}
		}
		stage('Test'){
			steps {
				echo "Test"	
			}
		}
		stage('Integration Test'){
			steps {
				echo "Integration Test"	
			}
		}
	}

	post{
		always{
			echo " This is a microservice"
		}
		success{
			echo " Execueted this step as the build is successfull"
		}

		failure{
			echo " Executed this step as the build failed"
		}
	}

}
