node {
	stage("checkout SCM") {
			checkout changelog: false, scm: [$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'BitCred', url: 'http://novartis.devops.altimetrik.io:7990/scm/son/ansible-roles.git']]]
		}
		stage("ansible-roles") {
			
			step([$class: 'AnsiblePlaybookBuilder', additionalParameters: '', ansibleName: 'ansibles', becomeUser: '', credentialsId: '', forks: 5, inventory: [$class: 'InventoryDoNotSpecify'], limit: '', playbook: 'playbook.yml', skippedTags: '', startAtTask: '', sudoUser: '', tags: '', vaultCredentialsId: ''])		
		}

}
	
