pipeline{
	// agent any
	agent {
		docker {image 'node:alpine'}
	}
	stages{
		stage("A Stage"){
			steps{
				echo "A Stage"
				sh 'node -v'
				}
			}
		stage("B Stage"){
				steps{
					echo "B Stage"
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