pipeline {
  agent {
    docker {
      image 'php'
    }

  }
  stages {
    stage('composer install') {
      agent any
      steps {
        sh 'composer install'
      }
    }
    stage('test') {
      steps {
        sh './vendor/bin/behat --format=progress --no-interaction'
      }
    }
  }
}