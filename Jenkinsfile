node('maven-label') {
   def mvnHome

   stage('Preparation') { // for display purposes
      // Get some code from a GitHub repository
     git 'https://github.com/sanders-fresco-pvt-ltd/Assignment_3.git' 
     // Get the Maven tool.
      // ** NOTE: This 'M3' Maven tool must be configured
      // **       in the global configuration.           
      mvnHome = tool 'M3'
   }
   
   stage('Compile') {
      // Run the maven build
      if (isUnix()) {
         sh "echo 'this was a semi-succesfull run'"
      } else {
         bat(/"${mvnHome}\bin\mvn" -Dmaven.test.failure.ignore clean package/)
      }
   }
   
   stage('Build') {
      sh ""
   }
   
   stage('Code Review') {
      sh ""
   }
   
   stage('Unit Test') {
      sh ""
   }

   stage('Package') {
      sh ""
   }
   stage('Deploy') {
      sh ""
   }


}
