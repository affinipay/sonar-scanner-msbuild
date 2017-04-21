pipeline {
  agent {
    node {
      label 'msbuild'
    }
    
  }
  stages {
    stage('error') {
      steps {
        bat(script: 'echo %PATH%', encoding: 'us-ascii')
      }
    }
  }
}