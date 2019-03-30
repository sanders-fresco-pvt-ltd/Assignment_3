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
   
   stage('Build') {
      sh "'${mvnHome}/bin/mvn' -Dmaven.test.failure.ignore clean package"
   }
   
   stage('Code Review') {
      sh "echo do some review"
   }
   
   stage('Unit Test') {
      sh "echo do some tests"
   }

   stage('Package') {
      sh "echo do some packaging"
   }
   stage('Deploy') {      
      //Copy the generated JenkinsWar file, on the Jenkins-Slave server, on to the Tomcat server 
      sh 'scp /home/vagrant/jenkins-agent/workspace/Example_Mvn/target/JenkinsWar.war root@192.168.32.20:/var/lib/tomcat7/webapps'
   }


}
