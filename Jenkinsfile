pipeline {
  agent any
    
  tools {nodejs "nodeJS"}
    
  stages {
        
    stage('Git Checkout') {
      steps {
        git branch: 'main', url: 'https://github.com/nejlalaayouni/angular.git'
      }
    }
     
    stage('Build') {
      steps {
        sh 'npm install'
         
      }
    }  
    
    stage('Start') {
      steps {
        sh 'npm run'
      }
    }
    stage('TEST') {
      steps {
        sh 'curl POST http://127.0.0.1:4200'
      }
    }
  }
  
}

