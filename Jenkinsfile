pipeline {
  agent any
  
  environment {
    GKE_PROJECT_ID = 'my-gke-project-378320'
    GKE_CLUSTER_NAME = 'gke-cluster-1'
    GKE_ZONE = 'us-east1-b'
  }
  
  stages {
    stage('Connect to GKE') {
      steps {
        // Authenticate to Google Cloud using a service account key.
        withCredentials([file(credentialsId: 'gcp-service-account-key', variable: 'SA_KEY')]) {
          sh 'gcloud auth activate-service-account --key-file=${SA_KEY}'
        }
        
        // Set the default Google Cloud project.
        sh "gcloud config set project ${GKE_PROJECT_ID}"
        
        // Set the current Google Cloud zone.
        sh "gcloud config set compute/zone ${GKE_ZONE}"
        
        // Connect to the GKE cluster.
        sh "gcloud container clusters get-credentials ${GKE_CLUSTER_NAME}"
      }
    }
    
    stage('Deploy to GKE') {
      steps {
        // This stage will deploy your application to the GKE cluster.
        // You can use kubectl commands or other tools to perform the deployment.
        // sh 'kubectl apply -f deployment.yaml'
        sh 'echo kubernetes deployment'
      }
    }
  }
}
