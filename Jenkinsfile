pipeline {
  agent any
  stages {
    stage('build-app') {
      steps {
        echo 'this is the build job'
        sh 'mvn compile'
      }
    }

    stage('test-app') {
      steps {
        echo 'this is the test job'
        sh 'mvn clean test'
      }
    }

    stage('package-app') {
      steps {
        echo 'this is the package job'
        sh 'mvn package -DskipTests'
      }
    }

    stage('Archive') {
      steps {
        archiveArtifacts '**/target/*.jar'
      }
    }

  }
  tools {
    maven 'maven'
  }
  post {
    always {
      echo 'Hey this is my Shopping-Cart pipeline.'
    }

  }
}