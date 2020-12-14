pipeline {
  agent any
  stages {
    stage('build code ') {
      steps {
        sh 'mvn clean package'
      }
    }
stage('static analysis ') {
      steps {
        sh ' echo "my new jenkins"'
      }
    }
    
    stage("build & SonarQube analysis") {
            agent any
            steps {
              withSonarQubeEnv('sonatrqube') {
                sh 'mvn clean package sonar:sonar'
              }
            }
          }
  }
}
