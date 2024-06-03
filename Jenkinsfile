pipeline {
    agent any
    stages {
      stage('build') {
        steps {
          git url: 'https://github.com/JonaxelN/AngularJenkinsTest.git', branch: 'main'
          sh '/usr/bin/ng build --prod'
        }
      }
      stage('Tar') {
        steps {
          //sh 'docker build -t luidasa/angular-app-jenkins:${VERSION}.${BUILD_NUMBER} .'
          sh 'tar -cvzf dist.tar.gz --strip-components=1 dist'
        }
      }
      stage('Gracias Totales') {
      steps {
        echo 'Gracias Totales'
      }
    }
    }
}