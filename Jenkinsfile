pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
              sh "docker image build -t wancloudsinc/flask_bravi ."
              sh "docker tag wancloudsinc/flask_bravi wancloudsinc/flask_bravi:beta"
              withCredentials([usernamePassword(
                  credentialsId: "docker",
                  usernameVariable: "aswadwc",
                  passwordVariable: "YjBkNzdlMjA3YWM4NmQ4NmUyODExNWNl"
              )]) {
                  sh "docker login -u $USER -p $PASS"
              }
              sh "docker image push wancloudsinc/flask_bravi:beta"
            }
        }
    }
}
