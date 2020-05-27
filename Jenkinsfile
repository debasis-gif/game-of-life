pipeline {
  agent {
    node {
      label 'MASTER'
    }

  }
  stages {
    stage('scm') {
      steps {
        git(url: 'https://github.com/debasis-gif/game-of-life.git', branch: 'master', credentialsId: 'jenkins', poll: true)
      }
    }

    stage('build') {
      steps {
        build 'mvn package'
        archiveArtifacts(artifacts: '*/target/*.war', onlyIfSuccessful: true)
      }
    }

  }
}