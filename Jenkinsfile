pipeline {
  agent any
  stages {
    stage('test') {
      agent {
        docker {
          image 'composer'
          args '--rm --interactive --tty --volume'
        }

      }
      steps {
        sh 'composer install'
      }
    }
  }
}