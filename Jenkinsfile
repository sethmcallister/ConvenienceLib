pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean install deploy'
      }
    }
  }

  tools {
    maven 'm2'
  }

  triggers {
    pollSCM('H/1 * * * *')
  }
}

