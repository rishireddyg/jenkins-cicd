node{
      stage('SCM Checkout'){
      git 'https://github.com/rishireddyg/jenkins-cicd.git'
      }
      
      stage('Compile Package'){
      def mvnHome = tool name: 'maven3', type: 'maven'
            sh "${mvnHome}/bin/mvn package"
      }
     	
}
