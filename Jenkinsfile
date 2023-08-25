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
               ansiblePlaybook credentialsId: 'Ansible', installation: 'Ansible', playbook: './apache2', inventory: './inventory'

            }
        }
    }
}

