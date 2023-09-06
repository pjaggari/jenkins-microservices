// Scripted
// node {
// 	echo "Build"
// 	echo "Test"
// 	echo "Integration Test"
// }

// Declarative

pipeline {
	//agent { docker {image 'maven:3.6.3'}}
	agent any

	environment {
		dockerHome = tool "myDocker"
		mavenHome = tool "myMaven"
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"

	}

	stages{
		stage('Build'){
			steps {
				//sh 'mvn --version'
				echo "Build"
				echo "Path - $Path"
				echo "Build Number - $env.BUILD_NUMBER"
				echo "Build ID - $env.BUILD_ID"	
				echo "Job Name - $env.JOB_NAME"
				echo "Build Tag - $env.BUILD_TAG"
				echo "BUILD URL - $env.BUILD_URL"
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
