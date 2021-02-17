pipeline {
	//agent any
agent { docker { image "maven:6.3.0"} }
	stages {

		stage('Build') {
			steps {

				echo "Build"
				sh "node --version"
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