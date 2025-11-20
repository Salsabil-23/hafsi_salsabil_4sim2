pipeline {
    agent any

    stages {
        stage('GIT') {
            steps {
                git url: 'https://github.com/Malekmouelh/devops.git'
            }
        }

        stage('Test Stage') {
            steps {
                    sh'mvn test'
            }
        }

        stage('Package Stage') {
            steps {
                sh 'mvn package '
            }
        }
    }

    post {
        success {
            echo 'build and tests succeded'
        }
        failure {
            echo 'build failed'
        }
    }
}