pipeline {
  agent any
  
  stages {
    stage('Get Nodes') {
      steps {
        sh '''
            /usr/local/bin/kubectl get nodes   
        '''
      }
    }
  }
}