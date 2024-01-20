pipeline {
    agent any

    stages {
        stage('docker build') {
            steps {
                sh 'docker build -t javaspring:v1 .'
            }
        }
      stage('docker tag') {
            steps {
                sh 'docker tag javaspring:v1 prasadchandu/nag:javaspring'
            }
        }
      stage('docker login') {
            steps {
                sh 'docker login'
            }
        }
      stage('docker push') {
            steps {
                sh 'docker push prasadchandu/nag:javaspring'
            }
        }
    }
}
