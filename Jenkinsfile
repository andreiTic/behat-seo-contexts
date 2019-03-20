pipeline {
  agent {
    docker {
      image 'php'
    }

  }
  stages {
    stage('composer install') {
      agent {
        docker {
          image 'composer'
          args '--tty --volume $PWD:/app'
        }

      }
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