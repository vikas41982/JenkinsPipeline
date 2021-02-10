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

    stage('Deployment') {
      steps {
        echo 'This is the deployment step'
      }
    }

    stage('Test') {
      steps {
        echo 'After the deployment, perform the test'
      }
    }

  }
}