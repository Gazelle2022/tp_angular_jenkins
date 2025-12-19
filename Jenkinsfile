pipeline {
    agent any

    triggers {
        githubPush()   
    }
//test for github webhook trigger
    stages {

        stage('push') {
            steps {
                git branch: 'main', url: 'https://github.com/Gazelle2022/tp_angular_jenkins.git'
            }
        }

        stage('build') {
            steps {
                bat 'npm install'
                bat 'ng build --prod'
            }
        }
        stage('test') {
            steps {
                bat 'ng test --watch=false --browsers=ChromeHeadless'
            }
        }
        stage('deploy') {
            steps {
                echo 'Deploying application...'
                // Add your deployment commands here
            }
        }
    }
    post {
        always {
            echo 'This will always run after the stages.'
        }
        success {
            echo 'The pipeline succeeded!'
        }
        failure {
            echo 'The pipeline failed.'
        }
    }
}



