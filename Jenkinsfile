node {
   stage ( 'SCM Checkout'){
     git 'https://github.com/janakiram213/game_of_life.git'
   }
   stage ('Compile-Package'){
     //get maven home path
      def mvnHome = tool name: ", type: 'maven'
      sh "${mvnHome}/bin/mvn package"
    }
}    
