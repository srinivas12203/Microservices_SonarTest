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
  }
    post {
    always {
      junit '**/build/test-results/**/TEST-*.xml'

    }

  }
  environment {
    gradle = '5.5-rc3'
  }
}
