node{
      stage('SCM Checkout'){
      git 'https://github.com/rishireddyg/jenkins-cicd'
      }
      
      stage('Compile Package'){
      def mvnHome = tool name: 'maven3', type: 'maven'
            sh "${mvnHome}/bin/mvn package"
      }
      stage('SonarQube Analysis'){
	     def mvnHome=tool name: 'maven' , type: 'maven'
	     withSonarQubeEnv('sonar-7'){
	     sh "${mvnHome}/bin/mvn sonar:sonar"
	    }
      stage('Slack Notification'){
            slackSend baseUrl: 'https://hooks.slack.com/services/', botUser: true, channel: 'rr-consultants', color: 'good',
                  message: 'welcome to slack', tokenCredentialId: 'slack-notification', username: 'rushendra'
      }
}
