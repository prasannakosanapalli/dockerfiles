node {
	stage("checkout SCM") {
		git changelog: false, credentialsId: 'github', url: 'https://github.com/prasannakosanapalli/dockerfiles.git'
		}
		stage("ansible-roles") {
			ansiblePlaybook installation: 'ansible', playbook: 'playbook.yml'
			
			}

}
	
