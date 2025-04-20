pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t macha-food-app .'
      }
    }
    stage('Test') {
      steps {
        sh 'docker run macha-food-app | grep "Biryani confirmed"'
      }
    }
    stage('Deploy') {
      steps {
        sh 'docker run -d macha-food-app'
      }
    }
  }
}
