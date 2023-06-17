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
        sh 'cd /home/frank/apps/next-blog/next-js-blog'
        sh '/home/frank/.nvm/versions/node/v16.14.2/bin/pm2 stop next-blog'
        sh 'git pull origin main'
        sh 'npm run build'
        sh '/home/frank/.nvm/versions/node/v16.14.2/bin/pm2 start next-blog'
      }
    }
  }
}