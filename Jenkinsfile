pipeline {
  agent { label 'jdk21' }

  tools {
    maven 'maven 3.9.9'
  }

  stages {
    stage('Stage1') {
      steps {
        echo 'Ejecucion stage 1'
      }
    }
    stage('Stage2') {
      steps {
        bat 'mvn --version'
      }
      post {
        always {
          echo 'dentro de stage 2'
        }
      }
    }
    stage('Stage3') {
      steps {
        echo 'Ejecucion stage 3'
      }
    }
  }

  post {
    always {
      echo 'al final'
    }
  }
}
