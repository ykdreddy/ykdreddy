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
                                playbook: 'apache2',
                                inventory: 'inventory'
            }
        }
    }
}

