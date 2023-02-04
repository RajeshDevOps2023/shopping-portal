pipeline {
  agent any
  stages {
    stage('build-the-app1') {
      steps {
        echo 'this is the build job'
        sh 'npm install'
      }
    }

    stage('test-the-app1') {
      steps {
        echo 'this is the test job'
        sh 'npm test'
      }
    }

    stage('package-the-app1') {
      steps {
        echo 'this is the package job'
        sh 'npm run package'
      }
    }

    stage('ArchiveStep') {
      steps {
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'this pipeline has completed...'
    }

  }
}