// Scripted
// node {
// 	echo "Build"
// 	echo "Test"
// 	echo "Integration Test"
// }

// Declarative

pipeline {
	agent { docker {image 'maven:3.6.3'}}
	stages{
		stage('Build'){
			steps {
				sh 'mvn --version'
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
