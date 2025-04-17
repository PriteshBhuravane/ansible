pipeline {
    agent any

    stages {
        stage('Deploy with Ansible') {
            steps {
                ansiblePlaybook playbook: 'deploy_app.yml', inventory: 'inventory'
            }
        }
    }
}
