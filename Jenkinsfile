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
                sh 'ansible-playbook nginx.yaml -i inventory'
            }
        }
    }
}

