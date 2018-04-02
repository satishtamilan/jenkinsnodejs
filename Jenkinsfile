node {
    def nodehome
   stage('clone Repository') {
      checkout scm 
      
   }
   stage('Building the Image') { 
      
         nodehome=docker.build("satishtamilan/jenkinsnodejsintegration")  
   }
   stage('Pushing the Image') { 
      
      docker.withRegistry('https://hub.docker.com','dockercredentials') 
      {
          nodehome.push(1.0)
      }
     
   }
   stage('Results') {
      echo 'success'
   }
}
