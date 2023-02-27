pipeline {
  agent any
//   environment{
//     USE_GKE_GCLOUD_AUTH_PLUGIN = 'True'
//   }
  stages {
    stage('Get Nodes') {
      steps {
        sh '''
            kubectl version --output=yaml
        '''
      }
    }
  }
}