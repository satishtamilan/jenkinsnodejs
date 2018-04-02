node {
   def mvnHome
   stage('Preparation') {
      checkout scm           
      mvnHome = tool 'maven_home'
   }
   stage('Build') {
      if (isUnix()) {
         sh "'${mvnHome}/bin/mvn' -Dmaven.test.failure.ignore clean package"
      } else {
         bat(/"${mvnHome}\bin\mvn" -Dmaven.test.failure.ignore clean package/)
      }
   }
   stage('Results') {
      echo 'success'
   }
}
