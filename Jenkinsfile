pipeline {
   agent any
   stages {
   stage('Test') {
     steps {
        sh 'su  admin'
        sh 'docker build .'
        sh 'svn --version'
     }
   }
  }
}