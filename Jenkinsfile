pipeline {
    agent any

    stages {
	   stage('SCM Checkout') {
	     steps {
          git 'https://github.com/noorwale/sonar.git'
		  }
        }

        stage('Build') { 
            steps {
                sh 'mvn install' 
            }
        }
        stage('code-analysis') {
            steps {
             script{
                withSonarQubeEnv(credentialsId: 'sonarqube_token') {
                        sh 'mvn sonar:sonar'
                }
            }    
            }
        }
    }        
	
}
    

