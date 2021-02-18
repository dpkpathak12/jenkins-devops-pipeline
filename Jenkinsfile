pipeline {
	agent any
//agent { docker { image "maven:6.3.0"} }
	environment {
		dockerHome = tool 'mydocker'
		mavenHome = tool 'mymaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {

		stage('Build') {
			steps {

				echo "Build"

				echo "BUILD_ID - $env.BUILD_ID"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "$PATH - $env.PATH"
				echo "JOB_ID - $env.JOB_ID"
				echo "JOB_URL - $env.JOB_URL"
				echo "BUILD_URL - $env.BUILD_URL"
				echo "docker --version"
				echo "mvn --version"
				echo "installation successful"
				}
		}
		stage('Test') {
				steps {
				echo "Test"
			}
		}
		stage('deploy') {
			steps {
				echo "deploy"
				}
		}
	}
}