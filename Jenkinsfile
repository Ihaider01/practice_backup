pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/Ihaider01/practice_backup.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    dockerImage = docker.build("jenkins-backup-app")
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    dockerImage.run('-v /d/README.txt:/data/README.txt -v /d/backup_devops:/data/backup_devops')
                }
            }
        }
    }
}
