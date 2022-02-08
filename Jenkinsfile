pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
          sh '''
            tmp_dir=$(mktemp -d)
            echo "Directpry created"
            git clone git@github.com:sameerkhan97/sorting-searching-algorithms.git $tmp_dir
            echo "Repository cloned"
            cd $tmp_dir
          '''
      }
    }
  }
}
