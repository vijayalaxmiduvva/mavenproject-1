pipeline {
    agent none

    stages {
        stage('Build') {
            agent { label 'slave' }
            steps {
                echo 'Building..'
                sh '''
                   cd /home/ubuntu/
                   pwd
                   ansible node -m ping
                   cd /home/ubuntu/playbook/	  
                   ansible-playbook deploy.yaml
                '''
            }
        }
    }
}
