pipeline {
	agent any
	stages {
		stage('Git Clone') {
			steps {
				git ([url: "https://github.com/samodev/terraform_ansible_apache.git", branch: 'master' ])
			}
		}
		stage('checkout') {
			steps { 
				 sh "git checkout master"
			}
		}
		stage('ansible-playbook') {
			steps {
				sh "ansible-playbook installApache.yml --extra-vars "ansible_sudo_pass=2secure"
			}
		}	
	}
}
