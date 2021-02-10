pipeline {
  agent any
  stages {
    stage('Code Checkout') {
      steps {
        echo 'Taking latest code from repo  '
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

    stage('Deployment On Dev') {
      parallel {
        stage('Deployment') {
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

    stage('Test on Dev') {
      parallel {
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