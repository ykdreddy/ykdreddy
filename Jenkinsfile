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
                ansiblePlaybook playbook: 'apache.yaml', inventory: 'inventory'
            }
        }
    }
}

