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
               ansiblePlaybook installation: 'Ansible', playbook: '/var/lib/jenkins/workspace/ansible-deployment/apache2.yaml', inventory: 
'/var/lib/jenkins/workspace/ansible-deployment/inventory'

            }
        }
    }
}


