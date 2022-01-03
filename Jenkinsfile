node
{def mavenHome = tool name:"maven.3.8.4"
 
    stage ("checkoutcode")
    {
        git credentialsId: 'b44aabd4-68b0-4155-bb49-be67763df5fc', url: 'https://github.com/mavenapp/maven-web-application.git'
        
    }
    
    stage ("mavenbuild")
    { 
       sh "${mavenHome}/bin/mvn clean package"
      }
    /* stage ('sonarQube')
     { 
         sh "${mavenHome}/bin/mvn sonar:sonar"
     } 
    stage ('nexus')
     {
         sh "${mavenHome}/bin/mvn clean deploy"
     }
     stage ('tomcat')
     {
        sshagent(['0fbf8cea-0854-4543-9068-2407fc84a60b']) 
        {
            sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@3.111.36.41:/opt/apache-tomcat-9.0.56/webapps/"
        }  
     }   */ 
}
