pipeline {
  agent any
  stages {
    stage('Config') {
      steps {
        sh '''
          git config --global user.name "sameerkhan97"
          git config --global user.email "khansam9730@gmail.com"
          
          echo "Configuration successfull"
        '''
      }
    }
    
    stage('Clone') {
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
     
    stage('Tagging') {
      steps {
        sh '''
          git tag -a v.0.09.0 -m "V0.09.0 release of Tanzu framework" 28b3ff46c1f62bd56cc9bb20a5ca415c7594d384
          echo "tag pushing"
          git push origin $tagName
          echo "tags pushed"   
        '''
      }
    }
    
    stage('Release Branch') {
      steps {
        sh '''
          git checkout -b release-0.09
          echo "created and switched branch"
          git push origin release-0.09
          echo "pushed release branch to origin"
        '''
      }
    }
    stage('Cleaning') {
      steps {
        sh '''
          rm -f $tmp_dir
          echo "temp directory deleted"
        '''
      }
    }
  }
}
