pipeline{
	agent any
	// agent {
	// 	docker {image 'node:alpine'}
	// }
	environment{
		dockerHome = tool 'myDocker'
		nodeHome = tool 'myNode'
		PATH = '$dockerHome/bin:$nodeHome/bin:$PATH'
	}
	stages{
		stage("A Stage"){
			steps{
				sh 'docker version'
				sh 'node -v'
				}
			}
		stage("B Stage"){
				steps{
					echo "$PATH"
					echo "$env.BUILD_NUMBER"
					echo "$env.BUILD_ID"
					echo "$env.JOB_NAME"
					sh 'docker ps'
				}
			}	
		stage("C Stage"){
				steps{
					echo "C Stage"
					echo "hola..!"
				}
			}	
	}
	post{
		always{
			echo "always"
		}
		success{
			echo "success"
		}
		failure{
			echo "failure"
		}
	}
}	