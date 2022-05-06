pipeline{
   agent any
   stages{
     stage("checkout code"){
     steps{
      git url:'https://github.com/vamsi0047/My-app.git'
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
     stage("docker build"){
     steps{
         sh'mv ./target/*.war .'
         sh 'sudo docker rmi myapp:1.0'
         sh'sudo docker build -t myapp:1.0 .'
     }
    } 
    stage("docker push"){
     steps{
         echo "pushing code to docker repo"
     }
    }
      stage("running container"){
     steps{
         sh 'sudo docker run -d -p 8080:8080 --name myapp myapp:1.0'
     }
    }
     
   }
}
}
