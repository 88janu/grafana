pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout your repository
                git 'https://github.com/tarundanda147/grafana.git'
            }
        }
        
        stage('Deploy with Ansible') {
            steps {
                ansiblePlaybook inventory: '/etc/ansible/hosts', playbook: '/etc/ansible/graf.yml', vaultTmpPath: ''
                }
            }
        }
    }
