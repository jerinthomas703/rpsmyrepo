pipeline {
    agent any
    stages {
        stage('Get_Playbook') {
            steps {
                git 'https://github.com/jerinthomas703/rpsmyrepo'
            }
        }
        stage('Run_Playbook') {
            steps {
                sh 'ansible-playbook playbook.yml'
            }
        }
    }
}
