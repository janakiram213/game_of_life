/*node {
   stage ('SCM Checkout'){
     git 'https://github.com/janakiram213/game_of_life.git'
   }
   stage ('validate'){
     //get maven home path
     def mvnHome = tool name: 'maven-3', type: 'maven'
     sh "${mvnHome}/bin/mvn validate"
    }

   stage ('Compile'){
     //get maven home path
     def mvnHome = tool name: 'maven-3', type: 'maven'
     sh "${mvnHome}/bin/mvn compile"
    }
   stage ('test'){
     //get maven home path
     def mvnHome = tool name: 'maven-3', type: 'maven'
     sh "${mvnHome}/bin/mvn test"
    }
   stage ('package'){
     //get maven home path
     def mvnHome = tool name: 'maven-3', type: 'maven'
     sh "${mvnHome}/bin/mvn package"
    }
  stage ('deploy to tomcat'){
      sshagent(['tomcat-dev']) {
          sh 'scp -o StrictHostKeyChecking=no target/*.war ec2-user@ansadmin:/home/ec2-user/apache-tomcat-7.0.94/webapps'
    }
  }
}    

