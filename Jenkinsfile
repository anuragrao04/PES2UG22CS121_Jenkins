pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build "PES2UG22CS121-1"
        sh "make"
      }
    }
    stage ('Test') {
      steps {
        sh "./hello_exec"
      }
    }
    stage ('Deploy') {
      steps {
        sh "echo 'full deployment is happening'"
      }
    }
  }
  post {
    failure {
      error "pipeline failed"
    }
  }
}
