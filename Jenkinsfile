pipeline {
   agent any
   stages {
   stage('Test') {
     steps {
        sh './test.sh'
        sh 'svn --version'
     }
   }
  }
}