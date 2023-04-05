pipeline {
  agent any
   stages {
     stage ('Sonar Scan'){
          container('build') {
                stage('Sonar Scan') {
                  withSonarQubeEnv('sonar') {
                  sh './mvn verify org.sonarsource.scanner.maven:sonar-maven-plugin:sonar -Dsonar.projectKey=devopsni3'
                }
                }
            }
        }
   }
}
