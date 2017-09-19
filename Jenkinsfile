pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
              sh "docker image build -t wancloudsinc/flask_bravi ."
              sh "docker tag wancloudsinc/flask_bravi wancloudsinc/flask_bravi:beta"
              sh "docker login -u aswadwc -p YjBkNzdlMjA3YWM4NmQ4NmUyODExNWNl"
              sh "docker image push wancloudsinc/flask_bravi:beta"
            }
        }
    }
}
