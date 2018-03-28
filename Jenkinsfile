pipeline { 
	agent any
	stages {
		stage('build app') {
			steps {
				println("npm install")
			}
		}
		stage('build docker image') {
			steps {
				println("docker build -t frontend .")
			}
		}
		stage('remove container') {
			steps {
				println("docker stop nodejscontainer")
			}
		}
		stage('run container') {
			steps {
				println("docker run")
			}
		}
	} 
}
