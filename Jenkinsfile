pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/PriteshBhuravane/ansible.git'
            }
        }

        stage('Deploy with Ansible') {
            steps {
                ansiblePlaybook playbook: 'ansible/deploy_app.yml', inventory: 'ansible/inventory'
            }
        }
    }
}
