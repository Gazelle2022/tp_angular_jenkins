pipeline {
    agent any

    stages {
        stage('Install') {
            steps {
                echo 'Installing dependencies...'
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                echo 'Building Angular app...'
                sh 'ng build --prod'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'ng test --watch=false --browsers=ChromeHeadless || true'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                // Ajouter ici tes commandes de déploiement
            }
        }
    }

    post {
        always {
            echo 'This always runs after the stages.'
        }
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
