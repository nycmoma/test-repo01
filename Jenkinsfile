pipeline{
  agent {label "any"}
  environment {
      GIT_COMMIT_SHORT = "${env.GIT_COMMIT}".take(8)
  }
  stages {
    stage('Test'){
      steps {
        sh('printenv|sort')
        sh """
          ls -lah *
        """
        script {
          sh "echo it seems working"
        }
      }
    }
  }
}
