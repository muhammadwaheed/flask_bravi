pipeline {
   agent any
   stages {
   stage('Build') {
     steps {
        echo 'Building..'
        sh 'docker build -t wancloudsinc/netorc:latest -f Dockerfile .'
        sh 'docker build -t wancloudsinc/netorc:nfdump -f Dockerfile .'
     }
   }
  }
}