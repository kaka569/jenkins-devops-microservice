//Declarative

pipeline{
	    agent any
		stages{
			stage('build'){
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