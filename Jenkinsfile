pipeline{
    agent any
    stages {
        stage("Checkout"){
        steps {
            checkout scm: [$class: 'GitSCM', userRemoteConfigs: [[url: 'https://github.com/r-kalyan-r/javaproject.git',credentialsId: 'git-token']], branches: [[name: 'main']]], poll: false
          }
        }
        stage("Main branch stage") {
            when {
                branch "main"
		    //   Runs only if the branch is "main"
            }
            steps {
                echo "Run main branch stage"
            }
        }
        stage("Develop branch"){
            when {
                branch "develop"
              // Runs only if the branch is "develop"       
            }
            steps {
                 echo "Run develop branch script"
		 }          
        }
	stage("Feature branch"){
            when {
                branch "feature-*"
  // run this stage  if the branch name starts with feature-
            }
            steps {
                 echo "Run Feature branch script"
                 }
        }
    }
}
