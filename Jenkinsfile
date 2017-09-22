pipeline {
   agent any
   stages {
   stage('Test') {
     steps {
        sh 'docker -t wancloudsinc/netorc-base -f Dockerfile .'
        sh 'svn --version'
     }
   }
  }
}