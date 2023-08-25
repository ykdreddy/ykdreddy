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
             echo "Executing command: /usr/bin/ansible/ansible-playbook ./apache2 -i ./inventory --private-key 
/var/lib/jenkins/workspace/ansible-deployment/ssh16448858192613577823.key -u ubuntu"
sh "/usr/bin/ansible/ansible-playbook ./apache2 -i ./inventory --private-key /var/lib/jenkins/workspace/ansible-deployment/ssh16448858192613577823.key -u ubuntu"


            }
        }
    }
}

