pipeline {
  agent {
    docker {
      image 'ubuntut'
    }
  }
 tools {
        maven 'MyMaven'
       
    }
    stages {
       

        stage ('Build') {
            steps {
                bat 'mvn -Dmaven.test.failure.ignore=true install' 
            }
            post {
                success {
                   echo 'Build completed succesfully'
                }
            }
        }
    }
}
