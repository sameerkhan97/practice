pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'cd ./Jenkins'
        sh 'chmod +x demo.sh'
        sh './demo.sh'
        // sh 'echo "Hello World"'
      }
    }
  }
}
