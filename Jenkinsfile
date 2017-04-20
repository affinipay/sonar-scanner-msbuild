pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        bat(script: 'build.cmd', encoding: 'us-ascii')
      }
    }
  }
}