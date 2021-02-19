pipeline {
	agent any
//agent { docker { image "maven:6.3.0"} }
	environment {
		dockerHome = tool 'mydocker'
		mavenHome = tool 'mymaven'
		PATH = "$dockerHome/bin:mavenHome/bin:$PATH"
	}
	stages {

		stage('checkout') {
			steps {
				//sh "docker version"
				//sh "mvn --version"
				
				echo "Build"

				echo "BUILD_ID - $env.BUILD_ID"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "$PATH - $env.PATH"
				echo "JOB_ID - $env.JOB_ID"
				echo "JOB_URL - $env.JOB_URL"
				echo "BUILD_URL - $env.BUILD_URL"
				
				echo "installation successful"
				}
		}
		stage('compile') {
				steps {

				sh "mvn clean compile"
			}
		}
		stage('test') {
			steps {
				sh "mvn test"	
					}
		}			
		stage('integration test') {
			steps {
				sh "mvn failsafe:integration-test failsafe:verify"	
					}
		}
	}
}