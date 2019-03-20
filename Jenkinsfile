pipeline {
  agent any
  stages {
    stage('install') {
      agent any
      steps {
        sh 'composer install && composer serve &> /dev/null &'
      }
    }
  }
}