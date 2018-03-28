pipeline { 
	agent any
	stages {
		stage('build app') {
			steps {
				println("npm install")
				sh '''npm install
				ng build
				'''

			}
		}
		stage('build docker image') {
			steps {
				println("docker build -t frontend .")
				sh '''docker build -t frontend .'''
				'''
			}
		}
		stage('remove container') {
			steps {
				println("docker stop nodejscontainer")
			sh '''docker stop docker-nodejs-instance-1 || true
			docker rm docker-nodejs-instance-1 || true '''
			}
		}
		stage('run container') {
			steps {
				println("docker run")
				sh '''docker run -d -p 80:80 --name docker-build-NodeJSApp frontend
				'''
			}
		}
	} 
}
