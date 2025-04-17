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
                LANG = 'en_US.UTF-8'
                LC_ALL = 'en_US.UTF-8'
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
