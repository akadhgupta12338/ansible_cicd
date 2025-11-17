pipeline {
    agent any
    
    stages {
        stage("SCM checkout") {
            steps {
                git https://github.com/akadhgupta12338/ansible_cicd.git'
            }
        }
        
        stage("Execute Ansible") {
            steps {
                ansiblePlaybook credentialsId: 'private-key',
                                 disableHostKeyChecking: true,
                                 installation: 'Ansible',
                                 inventory: 'inventory.yaml',
                                 playbook: 'nginx.yaml'
            }    
        }    
    }
}
