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
              ansiblePlaybook installation: 'Ansible', playbook: 'apache2.yaml', inventory: 'inventory'

            }
        }
    }
}


