pipeline {
  agent any
    
  tools {nodejs "NodeJS"}
    
  stages {
     
    stage('Build') {
      steps {
        sh 'npm install'
         sh 'npm run build'
      }
    }  
    
            
    stage('Deploy') {
      steps {
        sh """
          sudo -u frank bash -c "cd /home/frank/apps/next-blog/next-js-blog && ./refresh.sh"
        """
      }
    }
  }
}