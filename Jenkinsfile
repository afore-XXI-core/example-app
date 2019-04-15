node {
	def app

	stage('Clone repository'){
		checkout scm
	}

	stage('Build image'){
		app = docker.build('afore-xxi-core/example-app')
	}

	stage('Push image'){
		docker.withRegistry('https://registry.hub.docker.com', 'push docker hub'){
			app.push('latest')
		}
	}
}