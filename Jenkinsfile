pipeline {
  agent any
  stages {
    stage('StopCrone') {
      steps {
        sh 'crontab -l'
      }
    }
    stage('StopServer') {
      steps {
        sh 'ssh crmao01 /srv/bin/crm///adm/shell/restart_servers.ksh -S STOP'
      }
    }
  }
}