pipeline {
    agent any
    stages {
        stage('Clonage du dépôt GitHub') {
            steps {
                git 'https://github.com/corentin-godefroy/StringInverser'
            }
        }
        stage('Build') {
            steps {
                script {
                    if (isUnix()) {
                        echo 'Running on Unix...'
                        sh 'make'
                    } else {
                        echo 'Running on Windows...'
                        bat 'make'
                    }
                }
            }
        }
    }
}
