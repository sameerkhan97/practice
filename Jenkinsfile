pipeline {
  agent any
  stages {
    stage('Build') {
      step{
        // sh './Jenkins/demo.sh'
        sh 'echo "Hello World"'
      }
    }
    stage('Deploy') {
      step{
        sh 'echo "Deploying"'
      }
    }
  }
}
