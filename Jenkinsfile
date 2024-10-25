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
                        sh 'make'
                        stage('Permissions'){
                            echo 'ok'
                        }
                    } else {
                        echo 'Running on Windows...'
                        bat 'make'
                    }
                }
            }
        }
    }
}
