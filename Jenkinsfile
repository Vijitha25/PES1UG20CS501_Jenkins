pipeline {
  agent any
  stages {
    stage('Build'){
      steps {
        sh 'g++ pes501.cpp -o pes501'
        echo 'Build successful'
      }
    }
    stage('Test') {
      steps {
        sh './pes501'
        echo 'Test stage successful'
      }
    }
    stage('Deploy'){
      steps {
        echo 'Deployment Successful'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline failed'
    }
  }
}
