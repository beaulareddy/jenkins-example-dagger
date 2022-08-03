pipeline {
  agent { label 'slave' }
  environment {
    DH_CREDS=credentials('dockerhub')
  }
  stages {
    stage("setup") {
      steps {
        sh '''
          dagger project init
          dagger project update
        '''
      }
    }
    stage("do") {
      steps {
        sh 'dagger do push --log-format=plain'
      }
    }    
  }
}
