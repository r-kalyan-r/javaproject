pipeline{
    agent any
    stages {
        stage("Checkout"){
        steps {
            checkout scm: [$class: 'GitSCM', userRemoteConfigs: [[url: 'https://github.com/r-kalyan-r/javaproject.git',credentialsId: 'git-token']], branches: [[name: 'main']]], poll: false
          }
        }
        stage("Shell script change") {
            when {
                changeset "*/*.sh"
		    // scan all the folders and check if there is change in shell script  
            }
            steps {
                echo "executing QA script"
            }
        }
        stage("python change"){
            when {
                changeset "*/*.py"
              // scan all the folders and check if there is change in python script       
            }
            steps {
                 echo "executing Prod script"
		 }          
        }
	stage("html change"){
            when {
                changeset "*/*.html"
  // scan all the folders and check if there is change in html file  
            }
            steps {
                 echo "executing Dev script"
                 }
        }
    }
}
