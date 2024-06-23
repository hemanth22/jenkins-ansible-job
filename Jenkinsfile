pipeline {
    agent none
    stages {
        stage('Download the github repository') {
            agent any
            steps {
                git branch: 'main', changelog: false, credentialsId: 'github_hemanth22', poll: false, url: 'https://github.com/hemanth22/jenkins-ansible-job.git'
            }
        }
        stage('Execute Ansibe') {
            agent any
            steps {
                sh 'ansible-playbook -vvvvv gather_os_info.yaml'
            }
        }
    }
}
