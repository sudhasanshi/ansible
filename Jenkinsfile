pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                sh 'rm -rf ansible'
                sh 'git clone https://github.com/sudhasanshi/ansible.git'
            }
        }
        
        stage('Run Ansible Playbook') {
            steps {
                // Execute Ansible playbook
                sh 'ansible-playbook -i inventory tomcat_playbook.yml'
            }
        }
    }
}
