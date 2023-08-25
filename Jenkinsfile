pipeline {
    agent any
    stages {
        stage("SCM clone") {
            steps {
                echo "clone"
            }
        }
        stage("Ansible deployment") {
            steps {
                ansiblePlaybook credentialsId: 'ansiblekey',
                                installation: 'Ansible',
                                playbook: 'apache2',
                                inventory: './inventory',
                                extras: "--private-key /home/ubuntu/.ssh/id_rsa.pub -u ubuntu"
            }
        }
    }
}

