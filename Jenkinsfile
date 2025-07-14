pipeline {
    agent {
        docker {
            image 'node:18'
        }
    }

    environment {
        SRC_FILE = '/data/README.txt'
        DEST_FOLDER = '/data/backup_devops'
    }

    stages {
        stage('Verify Paths') {
            steps {
                sh 'echo "Backing up $SRC_FILE to $DEST_FOLDER"'
                sh 'ls -l /data'
            }
        }

        stage('Copy File') {
            steps {
                sh 'cp $SRC_FILE $DEST_FOLDER'
            }
        }
    }
}
