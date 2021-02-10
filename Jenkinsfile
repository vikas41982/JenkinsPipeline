pipeline {
  agent any
  stages {
    stage('Code Checkout') {
      steps {
        echo 'Taking latest code from repo'
        input(message: 'Are you sure, you want to start', id: 'Ok')
      }
    }

    stage('Restore') {
      steps {
        echo 'This is the step for restoring the references/nuget packages'
      }
    }

    stage('Compilation') {
      steps {
        echo 'This is the code compilation step.'
      }
    }

    stage('Deployment') {
      parallel {

        stage('Deployment on Dev') {
          steps {
            echo 'This is the deployment step'
          }
        }

        stage('Deployment on QA') {
          steps {
            echo 'This step will deploy code on QA site'
          }
        }

      }
    }

    stage('Test') {
      parallel {
        when { branch 'development' }
        stage('Test on Dev') {
          steps {
            echo 'After the deployment, perform the test'
          }
        }

        stage('Test On QA') {
          steps {
            echo 'This step will test code on QA site'
          }
        }

      }
    }

  }
}