pipeline {
    agent any

    stages {
        stage('GIT') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Salsabil-23/hafsi_salsabil_4sim2.git'
            }
        }

        stage('Test Stage') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package Stage') {
            steps {
                sh 'mvn package'
            }
        }
    }

    post {
        success {
            echo 'build and tests succeeded'
        }
        failure {
            echo 'build failed'
        }
    }
}