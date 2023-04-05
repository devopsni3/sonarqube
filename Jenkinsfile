pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn verify org.sonarsource.scanner.maven:sonar-maven-plugin:sonar -Dsonar.projectKey=devopsni3'
      }
    }
    stage('SonarQube analysis') {
      steps {
        withSonarQubeEnv('SonarCloud') {
          sh 'mvn sonar:sonar'
        }
      }
    }
  }
}
