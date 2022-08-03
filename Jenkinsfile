pipeline {
  agent { label 'slave' }
  stages {
    stage('verify installation') {
      steps {
        sh '''
          ./bin/dagger version
          docker version
        '''
      }
    }
  }
}
