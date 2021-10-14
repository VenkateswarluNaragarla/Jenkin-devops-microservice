//SCRIPTED APPROCH
// node {
	
// 		echo "Build"
// 		echo "Test"
// 		echo "Intergration Test"
// }

//Declarative pipeline
pipeline {
	//agent any
	agent { docker {image 'maven:3.6.3'}}
	stages {
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