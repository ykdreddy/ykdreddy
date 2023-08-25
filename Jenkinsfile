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
                ansiblePlaybook installation: 'Ansible', inventory: 'inventory', playbook: 'apache2.yaml'
            }
        }
    }
}


