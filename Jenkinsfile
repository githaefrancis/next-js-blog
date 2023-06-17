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

          dir('/home/frank/apps/next-blog/next-js-blog') {
        sh 'pm2 stop next-blog'
        sh 'git pull origin main'
        sh 'npm run build'
        sh 'pm2 start next-blog'        
      }

      }
    }
  }
}