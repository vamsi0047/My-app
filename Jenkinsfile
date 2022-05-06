pipeline{
   agent any
   stages{
     stage("checkout code"){
     steps{
      git url:'https://github.com/vamsi0047/My-ap.git'
     }
     }
     stage("testing"){
       steps{
          sh 'mvn clean test'
       }
     
     }
     stage("building"){
       steps{
          sh 'mvn package'
       }
     
     }
     stage("sonarqube"){
     steps{
       withSonarQubeEnv(installationName: 'Sonarserver',credentialsId:'newSonar') {
          sh 'mvn sonar:sonar'
     }
    } 
     
   }
}
}
