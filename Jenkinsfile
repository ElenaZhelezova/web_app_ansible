pipeline {
    agent any

    stages {
        stage('Cloning our Git') {
            steps {
                git 'https://github.com/ElenaZhelezova/web_app_ansible.git'
            }
        }

        stage('Run playbook') {
            steps {
                ansiblePlaybook(credentialsId: 'admin', inventory: 'hosts.yml',
                playbook: 'web_app_playbook.yml', disableHostKeyChecking: true)
            }
        }
    }
}