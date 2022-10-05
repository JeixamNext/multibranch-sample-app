pipeline {
  agent any
  options {
    buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')
    disableConcurrentBuilds()
  }
  stages {
    stage('Build') {
      steps {
        echo "holita hola"
      }
    }
    stage('cat README') {
      when {
        branch "pruebas" // solo las de pruebas imprimiran el readme
      }
      steps {
        sh '''
          cat README.md
        '''
      }
    }
  }
}
