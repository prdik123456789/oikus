pipeline {
  agent any
  stages {
    stage('StopCrone') {
      steps {
        sh 'crontab -l'
      }
    }
    stage('StopServer - crmpao01') {
      parallel {
        stage('StopServer - crmpao01') {
          steps {
            sh 'ssh crmpao01 /srv/bin.../restart_servers.ksh'
          }
        }
        stage('stopServer crmpao02') {
          steps {
            sh 'ssh crmpao02 /srv/.../restart_servers.ksh'
          }
        }
      }
    }
    stage('StopDB jobs') {
      steps {
        sh 'stop db jobs'
      }
    }
  }
}