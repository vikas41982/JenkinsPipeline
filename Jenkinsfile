pipeline {
  agent any
  stages {
    stage('Code Checkout') {
      steps {
        echo 'Taking latest code from repo  '
        git(url: 'https://github.com/vikas41982/JenkinsPipeline.git', branch: 'master')
      }
    }

  }
}