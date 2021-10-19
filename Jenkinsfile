//SCRIPTED APPROCH
// node {
	
// 		echo "Build"
// 		echo "Test"
// 		echo "Intergration Test"
// }

//Declarative pipeline
pipeline {
	agent any
	//agent { docker {image 'maven:3.6.3'}}
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}

	stages {
		stage('Build'){
			steps {
				//echo 'mvn --version'
				echo "Build"
				echo " PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
			    echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_TAG - $env.BUILD_TAG"
			}
		}
		stage('Test'){
			steps {
				echo "Test"
			}
		}
		stage('Intergration Test'){
			steps {
				echo "Integration Test"
			}
		}
	} 
	post{
		always {
			echo " i am Awesome. I run always"
		} 
		success {
			echo "I run when you are success"
		}
	}

}