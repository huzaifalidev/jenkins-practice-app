pipeline {
  agent any

  stages {
    stage('Show HTML') {
      steps {
        echo 'Displaying index.html content:'
        sh 'cat index.html'
      }
    }

    stage('Deploy (Copy to folder)') {
      steps {
        sh 'mkdir -p deploy && cp index.html deploy/'
        echo 'index.html copied to deploy folder.'
      }
    }
  }

  post {
    success {
      echo 'Build finished successfully!'
    }
  }
}
