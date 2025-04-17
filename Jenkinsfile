pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Deploy with Ansible') {
            environment {
                PYTHONIOENCODING = 'utf-8'
            }
            steps {
                ansiblePlaybook(
                    playbook: 'deploy_app.yml',
                    inventory: 'inventory'
                )
            }
        }
    }
}
