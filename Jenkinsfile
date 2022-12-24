pipeline {
    agent any

    stages {
	   stage('SCM Checkout'){
	    steps {
          git 'https://github.com/noorwale/sonar.git'
		  }
        }

        stage('Build') { 
            steps {
                sh 'mvn install' 
            }
        }        
		
		
		  }

   }
    

