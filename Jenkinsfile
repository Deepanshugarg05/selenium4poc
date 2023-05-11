pipeline {
  agent any
  stages {
    stage('Selenium HUB up') {
      steps {
        sh 'step([$class: \'DockerComposeBuilder\', dockerComposeFile: \'docker-compose.yml\', option: [$class: \'StartAllServices\'], useCustomDockerComposeFile: false])'
      }
    }

    stage('Selnium Hub Down') {
      steps {
        sh 'docker compose -f docker-compose-v3-seleniumgrid.yml down'
      }
    }

  }
}