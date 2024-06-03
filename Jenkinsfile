pipeline {
    agent any
    tools {nodejs "nodejs"}
    stages {
      stage('build') {
        steps {
         echo 'Building'
        }
      }
      stage('Export') {
        steps {
          //sh 'docker build -t luidasa/angular-app-jenkins:${VERSION}.${BUILD_NUMBER} .'
          echo 'exporting'
        }
      }
      stage('Finish') {
      steps {
        echo 'Finish'
      }
    }
    }
}