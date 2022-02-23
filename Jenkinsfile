pipeline {
  agent any
  stages {
    stage('compile') {
      steps {
        echo 'this is the compile the app job'
        sh 'npm install'
      }
    }

    stage('test') {
      steps {
        echo 'this is the test the app job'
        sh 'npm test'
      }
    }

    stage('package') {
      steps {
        echo 'this is the package the app job'
        sh 'npm run package'
      }
    }

    stage('archive-app') {
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
      echo 'SUCCESS! this pipeline has completed...'
    }

  }
}