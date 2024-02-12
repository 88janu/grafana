pipeline {
  agent any
  
  stages {
    stage('checkout stage') {
      steps {
        sh 'rm -rf Ansible_project'
        sh 'git clone https://github.com/tarundanda147/grafana.git'
      }
    }
    stage('running playbook') {
      steps {
        sh 'ansible-playbook -i hosts graf.yml'
      }
    }
  }
}
