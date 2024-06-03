pipeline {
  agent any
  
  stages {
    stage('Iniciando') {
      steps {
        echo 'Hola Mundo'
      }
    }
    stage('Checkout') {
        checkout scm
    }
    stage('NPM Install') {
        withEnv(["NPM_CONFIG_LOGLEVEL=warn"]) {
            sh 'npm install'
        }
    }
    stage('Build') {
      sh 'ng build --prod --aot --sm --progress=false'
    }
    stage('Archive') {
      sh 'tar -cvzf dist.tar.gz --strip-components=1 dist'
      archive 'dist.tar.gz'
    }
    stage('Gracias Totales') {
      steps {
        echo 'Gracias Totales'
      }
    }
   }
}