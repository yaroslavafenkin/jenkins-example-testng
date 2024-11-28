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
      junit 'target/surefire-reports/*.xml'
    }
  }
}
