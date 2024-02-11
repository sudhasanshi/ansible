pipeline {
    agent any
    stages {
        stage('ansible') {
            steps {
		sh 'rm -rf ansible'
                sh 'git clone https://github.com/sudhasanshi/ansible.git'
            }
        }
		stage('deploy') {
            steps {
                sh 'ansible-playbook tomcat_playbook.yml -i /etc/ansible/hosts --private-key ~/.ssh/id_rsa --user root'
            }
        }
    }
}
