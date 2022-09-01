pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       maven 'maven' 
    }
   

    stages{
        stage('build-app'){
            steps{
                echo 'this is the build job'
                sh 'mvn compile'
            }
        }
        stage('test-app'){
            steps{
                echo 'this is the test job'
                sh 'mvn clean test'
            }
        }
        stage('package-app'){
            steps{
                echo 'this is the package job'
                sh 'mvn package -DskipTests'
            }
        }
    }
    
    post{
        always{
            echo 'Hey this is my Shopping-Cart pipeline.'
        }
        
    }
  }


