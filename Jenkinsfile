/* Jenkins Declarative Pipeline */
pipeline {
    agent {label 'MASTER'}

    stages {
        stage('Source') {
            steps {
                git 'https://github.com/debasis-gif/game-of-life.git'
            }
        }
        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}