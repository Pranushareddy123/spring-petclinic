pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        sh './mvnw clean compile'
      }
    }

    stage('Static Analysis') {
      steps {
        sh '''mvn sonar: sonar \\
  -Dsonar.projectKey=Petclinic \\
  -Dsonar.host.url=http://65.0.56.143:9000 \\
  -Dsonar.token=sqp_13c37d2ac4216f35aa6224854803460bc8783c68'''
      }
    }

  }
}