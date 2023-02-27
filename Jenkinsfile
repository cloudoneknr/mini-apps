pipeline {
  agent any
//   environment{
//     USE_GKE_GCLOUD_AUTH_PLUGIN = 'True'
//   }
  stages {
    stage('Get Nodes') {
      steps {
        sh '''
            /Users/nrkodari/Library/Application\ Support/cloud-code/installer/google-cloud-sdk/bin/kubectl version --output=yaml
        '''
      }
    }
  }
}