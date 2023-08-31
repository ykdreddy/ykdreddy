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
                sh 'ansible-playbook remove.yaml -i inventory --user jenkins --key-file ~/.ssh/id_rsa'
            }
        }
    }
}

