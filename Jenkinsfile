pipeline {
  agent any
  stages {
    stage('test') {
      agent {
        docker {
          image 'composer/composer'
        }

      }
      steps {
        sh 'composer install'
      }
    }
  }
}