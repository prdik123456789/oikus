pipeline {
  agent any
  stages {
    stage('StopCrone') {
      steps {
        sh 'crontab -l'
      }
    }
    stage('StopServers') {
      parallel {
        stage('crmpao01') {
          steps {
            sh 'ssh crmpao01 /srv/bin.../restart_servers.ksh'
          }
        }
        stage('crmpao02') {
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