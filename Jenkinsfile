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
        sh  './home/frank/apps/next-blog/next-js-blog/refresh.sh'
  
      }
    }
  }
}