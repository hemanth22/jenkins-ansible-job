pipeline {
    agent none
    stages {
        stage('Download the github repository') {
            steps {
                git branch: 'main', changelog: false, credentialsId: 'github_hemanth22', poll: false, url: 'https://github.com/hemanth22/jenkins-ansible-job.git'
            }
        }
        stage('Execute Ansibe') {
            steps {
                sh 'ansible-playbook gather_os_info.yaml'
            }
        }
    }
}
