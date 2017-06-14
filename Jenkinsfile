node {
  def mvnHome
   stage('Preparation') { // for display purposes
      // Get some code from a GitHub repository
       git credentialsId: 'a40f1393-6491-4406-a7a9-68a7d21ad703', url: 'git@github.com:Nieo/romannumerals.git'
      // Get the Maven tool.
      // ** NOTE: This 'M3' Maven tool must be configured
      // **       in the global configuration.           
   }
   stage('Build') {
      // Run the maven build
      if (isUnix()) {
         sh "mvn -Dmaven.test.failure.ignore clean package"
      }
   }
   stage('Results') {
      junit '**/target/surefire-reports/TEST-*.xml'
      archive 'target/*.jar'
   }
}
