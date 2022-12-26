pipeline{
    agent any
    stages {
        stage("Checkout"){
        steps {
            checkout scm: [$class: 'GitSCM', userRemoteConfigs: [[url: 'https://github.com/r-kalyan-r/javaproject.git',credentialsId: 'git-token']], branches: [[name: 'main']]], poll: false
          }
        }
        stage("main branch script ") {
            when {
                branch "main"
		    // Build only when main branch  
            }
            steps {
	             script {
                       def pom = readMavenPom file: 'pom.xml'
                       env.version = pom.version
                       echo "${pom.version}"
                       echo "${env.version}"
                }
            }
        }
        stage("develop branch script"){
            when {
                branch "develop"
              // scan all the folders and check if there is change in python script       
            }
            steps {
	                      script {
                       def pom = readMavenPom file: 'pom.xml'
                       env.version = pom.version
                       echo "${env.version}"
                }

		 }          
        }
	stage("feature branch script"){
            when {
                branch "feature-*"
  // builds on when branch starts with feature-  
            }
            steps {
	           script {
                       def pom = readMavenPom file: 'pom.xml'
                       env.version = pom.version
                       echo "${env.version}"
                 }
        }
    }
}
