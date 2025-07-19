pipeline {
  agent {
    node {
      label 'w1'
    }

  }
  stages {
    stage('echo') {
      steps {
        echo 'Hello to PIP-SUM Repo'
      }
    }

    stage('get-repo') {
      steps {
        git(url: 'https://github.com/saadelkenawy/pip-sum.git', branch: 'masin')
      }
    }

    stage('build phase') {
      steps {
        echo 'build'
      }
    }

    stage('build-process') {
      steps {
        sh '''chmod +x ./pip-sum.sh
./pip-sum.sh'''
      }
    }

    stage('Archive the artifact') {
      steps {
        archiveArtifacts 'output.txt'
        archiveArtifacts 'output.txt'
      }
    }

  }
}