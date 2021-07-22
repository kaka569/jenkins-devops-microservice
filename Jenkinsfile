//Declarative

pipeline{
	    agent any	
		environment{
			dockerhome = tool 'mydocker'
			mavenhome = tool 'mymaven'
		    PATH = "$dockerhome/bin:$mavenhome/bin:$PATH"
		}	
		stages{
			stage('checkout'){
				steps {
					sh 'mvn --version'
		           echo "Build"
				   echo "PATH - $PATH"
				   echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				   echo "BUILD_ID - $env.BUILD_ID"
				   echo "BUILD_TAG - $env.BUILD_TAG" 
				   echo "BUILD_URL - $env.BUILD_URL"
				   echo "JOB_NAME - $env.JOB_NAME"
				}
			}
			stage('compile'){
				steps{
					sh 'mvn clean compile'
				}
			}

			stage('Test'){
				steps {		           
		           sh 'mvn test'
				}
			}
			stage('Integration Test'){
				steps {	
		           sh 'mvn failsafe:integration:test'

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