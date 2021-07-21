//Declarative

pipeline{
	    //agent any
		agent { any { image 'maven:3.6.3'}}
		stages{
			stage('build'){
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
				echo "im awesome.i run always."
			}
			success{
				echo "i run when you are successful"
			}
			failure{
				echo "i run when you fail"
			}
		}
}