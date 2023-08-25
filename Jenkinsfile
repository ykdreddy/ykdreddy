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
#                ansiblePlaybook installation: 'Ansible', inventory: 'inventory', playbook: 'apache2.yaml'
                 ansiblePlaybook installation: 'Ansible', playbook: '/var/lib/jenkins/workspace/ansible-deployment/apache2.yaml', inventory: 
'/var/lib/jenkins/workspace/ansible-deployment/inventory'

            }
        }
    }
}


