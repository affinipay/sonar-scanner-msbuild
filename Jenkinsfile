pipeline {
  agent {
    node {
      label 'msbuild'
    }
    
  }
  stages {
    stage('error') {
      steps {
        bat(script: 'build.cmd', encoding: 'us-ascii')
      }
    }
  }
}