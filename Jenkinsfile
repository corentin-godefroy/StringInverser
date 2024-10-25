pipeline {
    agent any
    stages {
        stage('Clonage du dépôt GitHub') {
            steps {
                git branch:'main', url:'https://github.com/corentin-godefroy/StringInverser'
            }
        }
        stage('Build') {
            steps {
                script {
                    if (isUnix()) {
                        echo 'Running on Unix...'
                        sh 'apt install make'
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
