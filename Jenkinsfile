pipeline {
  agent any
  stages {
    stage('Selenium HUB up') {
      steps {
        sh 'step([$class: \'DockerComposeBuilder\', dockerComposeFile: \'docker-compose-v3-seleniumgrid.yml\', option: [$class: \'StartAllServices\'], useCustomDockerComposeFile: true])'
      }
    }

    stage('Selnium Hub Down') {
      steps {
        sh 'docker compose -f docker-compose-v3-seleniumgrid.yml down'
      }
    }

  }
}