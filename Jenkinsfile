//SCRIPTED APPROCH
// node {
	
// 		echo "Build"
// 		echo "Test"
// 		echo "Intergration Test"
// }

//Declarative pipeline
pipeline {
	agent any
	stages {
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