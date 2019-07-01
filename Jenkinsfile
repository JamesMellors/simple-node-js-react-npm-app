pipeline {
	agent {
		docker {
			image 'node:6-alpine'
			arge '-p 3000:3000'
			}
		}
	stages {
		stage('Build') {
			steps {
				sh 'npm install'
				}
		}
	}
}
