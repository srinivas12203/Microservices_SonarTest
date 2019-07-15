pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'gradle'
      }
    }
    stage('Code Test') {
      steps {
        sh 'gradle test'
      }
    }
    stage('Code Check') {
      steps {
        sh 'gradle check'
      }
    }
  }
  environment {
    gradle = '5.5-rc3'
  }
  post {
    always {
      junit '**/build/test-results/**/TEST-*.xml'

    }

  }
}