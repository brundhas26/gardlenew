pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                url: 'https://github.com/brundhas26/gardlenew.git'
            }
        }

        stage('Build') {
            steps {
                sh 'gradle build'
            }
        }

        stage('Test') {
            steps {
                sh 'gradle test'
            }
        }
    }

    post {
        success {
            echo 'Gradle Build Successful!'
        }

        failure {
            echo 'Gradle Build Failed!'
        }
    }
}
