pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh './Jenkins'
        sh 'chmod +x demo.sh'
        sh './demo.sh'
        // sh 'echo "Hello World"'
      }
    }
  }
}
