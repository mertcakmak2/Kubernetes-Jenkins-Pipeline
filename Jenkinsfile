pipeline {

  agent any

  stages {

      stage ('Prepare') {
            steps {
                echo "started build."
            }
      }
    
    stage('Deploy App on Kubernetes Cluster') {
      steps {
        script {
          kubernetesDeploy(configs: "deployment.yml", kubeconfigId: "mykubeconfig")
        }
      }
    }

  }

}