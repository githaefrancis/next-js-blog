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
        
        cd /home/frank/apps/next-blog/next-js-blog &&
        sh git pull origin main &&
        npm run build &&
        pm2 restart all

        """
      }
    }
  }
}