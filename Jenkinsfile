pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build is completed'
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Test stage is completed '
          }
        }

        stage('Test 2') {
          steps {
            echo 'Test stage two is completed'
          }
        }

      }
    }

    stage('Deploy Stage') {
      steps {
        input(message: 'Are you sure to completed ?', ok: 'yes, i will do it')
        echo 'Deploy is Completed'
      }
    }

    stage('Notify for new Deploy') {
      steps {
        input(message: 'Are you Sure', ok: 'Yes')
      }
    }

  }
}