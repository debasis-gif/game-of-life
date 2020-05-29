/* Jenkins Declarative Pipeline 2 */
pipeline {
    agent {label 'MASTER'}
    triggers { 
        upstream(upstreamProjects: 'GOL-delcarative-pipeline', threshold: hudson.model.Result.SUCCESS)
    } 
    stages {
        stage('Source') {
            steps {
                git branch: 'master', url: 'https://github.com/debasis-gif/game-of-life.git'
            }
        }
        stage('Package') {
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
                echo 'Successfully called GOL-declarative-pipeline2 after completing earlier job - GOL-declarative-pipeline'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}