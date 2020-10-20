pipeline {
 agent any
 environment {
  PATH = "/usr/share/maven/bin:$PATH"
 }
  stages {  
    stage('Maven Build Package'){
       steps {
        sh "mvn clean package"
      }
    }
   
  }
}
