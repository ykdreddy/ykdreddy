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
                ansiblePlaybook credentialsId: 'ubuntu',
                                installation: 'Ansible',
                                playbook: 'apache.yml',
                                inventory: './inventory',
                                extras: "--private-key /home/ubuntu/.ssh/id_rsa.pub -u ubuntu"
            }
        }
    }
}

