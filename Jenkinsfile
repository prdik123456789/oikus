pipeline {
  agent any
  stages {
    stage('StopCrone') {
      steps {
        sh 'crontab -l'
      }
    }
  }
}