pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/franklynux/helm-web-app.git'
          }
        }

        stage('Deploy with Helm') {
            steps {
                script {
                    bat 'C:\\ProgramData\\chocolatey\\bin\\helm.exe upgrade --install my-webapp ./webapp --namespace default'
                }
            }
        }
    }
}
