pipeline {
  agent any

  stages {

      stage('Build Artifact') {
            steps {
              sh "mvn clean package -DskipTests=true"
              archive 'target/*.jar' ///trying 2nd time for webhook
            }
        }

      stage('Unit Test') {
            steps {
              sh "mvn test"
              }
        }   
    }
}