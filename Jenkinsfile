pipeline {
  agent any
  environment{
    USE_GKE_GCLOUD_AUTH_PLUGIN = 'True'
  }
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