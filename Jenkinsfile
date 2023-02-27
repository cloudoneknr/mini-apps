pipeline {
  agent any
  environment{
    export USE_GKE_GCLOUD_AUTH_PLUGIN = 'True'
  }
  stages {
    stage('Get Nodes') {
      steps {
        sh '''
            /usr/local/bin/kubectl version --output=yaml
        '''
      }
    }
  }
}