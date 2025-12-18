pipeline {
  agent any

  tools { nodejs 'nodejs' }

  stages {
    
    stage('Cloning Git') {
      steps {
        git branch: 'main',  url: 'https://github.com/Gazelle2022/tp_angular_jenkins.git'
      }
    }
    


    stage('Install dependencies') {
      steps {
        bat 'npm install'
      }
    }
  }
}