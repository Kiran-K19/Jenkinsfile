/**
maven and gradle are build tools for backend
npm and yarn are build tools for frontend

Install these build tools as plugins in jenkins and configure them

All build tools will be available in global tool configurations
**/

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
   stage('run frontend') {
    steps {
     echo 'executing yarn...'
     nodejs('Node-10.17'){   /** install nodeJS plugin and pass yarn or npm in global tool config **/
       sh 'yarn install'
     }
    }
   }
 stage('run backend'){
  steps{
   echo 'executing gradle...'
   withGradle(){
    sh './gradlew -v'
   }
  }
 }
}
}
