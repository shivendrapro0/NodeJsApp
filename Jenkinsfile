pipeline { 
	stages {
		stage('build app') {
			println("npm install")
		}
		stage('build docker image') {
			println("docker build -t frontend .")
		}
		stage('remove container') {
			println("docker stop nodejscontainer")
		}
		stage('run container') {
			println("docker run")
		}
	} 
}
