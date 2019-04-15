node {
	def app

	stage('Clone repository'){
		checkout scm
	}

	stage('Build image'){
		app = docker.build('afore-xxi-core/example-app')
	}

	stage('Push image'){
		docker.withRegistry('https://registry.hub.docker.com', 'Credenciales hacia GitHub'){
			app.push('latest')
		}
	}
}