node{
      stage('SCM Checkout'){
      git 'https://github.com/rishireddyg/jenkins-cicd'
      }
      
      stage('Compile Package'){
      def mvnHome = tool name: 'maven3', type: 'maven'
            sh "${mvnHome}/bin/mvn package"
      }
      
      stage('Email Notification'){
            mail bcc: '', body: 'welcome to jenkins this is rishi', cc: '', from: '', replyTo: '', subject: 'welcome to jenkins test', to: 'rishireddy.devops@gmail.com'
      }
      
}
