pipeline { 
	stages {
		stage('build app') {
			step {
				println("npm install")
			}
		}
		stage('build docker image') {
			step {
				println("docker build -t frontend .")
			}
		}
		stage('remove container') {
			step {
				println("docker stop nodejscontainer")
			}
		}
		stage('run container') {
			step {
				println("docker run")
			}
		}
	} 
}
