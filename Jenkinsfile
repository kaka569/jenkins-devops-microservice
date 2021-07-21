//Declarative

pipeline{
	    agent any		
		stages{
			stage('build'){
				steps {
		           echo "Build"
				   echo "PATH - $PATH"
				   echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				   echo "BUILD_ID - $env.BUILD_ID"
				   echo "BUILD_TAG - $env.BUILD_TAG" 
				   echo "BUILD_URL - $env.BUILD_URL"
				   echo "JOB_NAME - $env.JOB_NAME"
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