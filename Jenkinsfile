pipeline {
  agent any
  stages {
    stage('Selenium HUB up') {
      steps {
        sh 'docker compose -f docker-compose-v3-seleniumgrid.yml up -  '
      }
    }

    stage('Selnium Hub Down') {
      steps {
        sh 'docker compose -f docker-compose-v3-seleniumgrid.yml down'
      }
    }

  }
}