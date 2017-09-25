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
   stage('Push') {
     steps {
        echo 'Pushing images on docker hub'
        sh 'docker login -u aswadwc -p YjBkNzdlMjA3YWM4NmQ4NmUyODExNWNl'
        sh 'docker push wancloudsinc/netorc:latest'
        sh 'docker push wancloudsinc/netorc:nfdump'
     }
   }
   stage('CleanUp') {
     steps {
        echo 'Removing images'
        sh 'docker rmi wancloudsinc/netorc:latest'
        sh 'docker rmi wancloudsinc/netorc:nfdump'
     }
   }
  }
}