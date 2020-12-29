pipeline{
   agent any
   parameters{
     choice(name:'branch', choices:['master','UAT','sprint'],defaultValue:'master')
     string(name:'name',defaultValue:'vamsi',description:'enter your name')
   }
   stages{
     stage("checkout code"){
     steps{
      git url:'https://github.com/vamsi0047/My-ap.git'
     }
     }
     stage("build the code"){
       steps{
          sh 'mvn clean test'
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
