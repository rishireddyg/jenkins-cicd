node{
      stage('SCM Checkout'){
      git 'https://github.com/rishireddyg/jenkins-cicd'
      }
      
      stage('Compile Package'){
      sh 'mvn package'
      }
}
