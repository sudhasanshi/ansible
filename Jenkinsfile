pipeline {
    agent any
    
    stages {
        stage('checkout') {
            steps {
                sh 'rm -rf ansible'
                sh 'git clone https://github.com/sudhasanshi/ansible.git'
            }
        }
        
        stage('execute') {
            steps {
                sh 'ansible-playbook -i inventory tomcat_playbook.yml'
            }
        }
    }
}
