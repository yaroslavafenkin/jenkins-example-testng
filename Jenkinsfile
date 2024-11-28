pipeline {
  agent any
  stages {
    stage('Run the tests') {
      steps {
        bat 'mvn clean test'
      }
    }
  }
  post {
    always {
      testNG reportFilenamePattern: 'target/surefire-reports/*.xml'
    }
  }
}
