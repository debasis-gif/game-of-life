/* Jenkins Declarative Pipeline */
pipeline {
    agent {label 'MASTER'}

    stages {
        stage('Source') {
            steps {
                git branch: 'master', url: 'https://github.com/debasis-gif/game-of-life.git'
            }
        }
        stage('Package') {
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
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