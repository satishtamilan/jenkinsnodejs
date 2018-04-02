node {
    def nodehome
   stage('clone Repository') {
      checkout scm 
      
   }
   stage('Building the Image') { 
      
         nodehome=docker.build("satishtamilan/jenkinsnodejsintegration")
     
   }
   stage('Test the Image') { 
      
        nodehome.inside(echo 'Test is passed')
     
   }
   stage('Pushing the Image') { 
      
      docker.withRegistry('http://hub.docker.com' 'dockercredentials') {app.push(1.0)}
     
   }
   stage('Results') {
      echo 'success'
   }
}
