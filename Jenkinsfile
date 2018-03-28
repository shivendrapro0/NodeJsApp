pipeline { 
	agent any
	stages {
		stage('build app') {
			steps {
				println("npm install")
				sh 'npm install'
				sh 'ng build'
			}
		}
		stage('build docker image') {
			steps {
			println("docker build -t frontend .")
			    def customImage = docker.build("frontend:latest")
    				customImage.inside {
        			sh 'echo i am frontend'
    				}
			}
		}
	} 
}
