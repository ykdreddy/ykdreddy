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
               sh "/usr/bin/ansible-playbook /var/lib/jenkins/workspace/ansible-deployment/apache2 -i /var/lib/jenkins/workspace/ansible-deployment/inventory 
--private-key 'Ansible' -u ubuntu"

            }
        }
    }
}

