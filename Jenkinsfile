pipeline {
  agent {
    docker 'ubuntu'
  }
 tools {
        maven 'MyMaven'
       
    }
    stages {
       

        stage ('Build') {
            steps {
                sh 'mvn -Dmaven.test.failure.ignore=true install' 
            }
            post {
                success {
                   echo 'Build completed succesfully'
                }
            }
        }
    }
}
