pipeline {
  agent any
  
  stages {
   stage('Install Dependencies') {
     steps {
       sh 'id'
       sh 'export|sort'
       sh 'npm install'
     }
   }
   stage('Build') {
     steps {
       sh 'npm run build'
     }
   }
  }
}