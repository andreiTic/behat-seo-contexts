pipeline {
  agent any
  stages {
    stage('test') {
      agent {
        docker {
          image 'composer'
          args '--rm --interactive --tty  --volume $PWD:/app'
        }

      }
      steps {
        sh 'composer install && composer serve &> /dev/null &'
      }
    }
    stage('tests') {
      agent {
        docker {
          image 'php'
        }

      }
      steps {
        sh './vendor/bin/behat --format=progress --no-interaction'
      }
    }
  }
}