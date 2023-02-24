pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'build completed'
      }
    }

    stage('Test stages') {
      parallel {
        stage('Test 2') {
          steps {
            echo 'Rainning Test 2'
          }
        }

        stage('Test1') {
          steps {
            echo 'rainning test 1'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Are you sure to deploy', ok: 'I am sure')
        echo 'completed deployement'
      }
    }

    stage('Notify your new build') {
      steps {
        echo 'notify new completed'
      }
    }

  }
}