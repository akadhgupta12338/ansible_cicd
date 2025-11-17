pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Checkout your code from a repository
                git 'your_repo_url'
            }
        }
        stage('Run Ansible Playbook') {
            steps {
                ansiblePlaybook(
                    colorized: true,
                    credentialsId: 'ssh-jenkins-key', // ID of the credentials you added
                    inventory: 'path/to/your/inventory.ini', // Path to your inventory file
                    playbook: 'path/to/your/playbook.yml', // Path to your playbook
                    sudo: true,
                    sudoUser: 'jenkins'
                )
            }
        }
    }
}
