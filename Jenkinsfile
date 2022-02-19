pipeline {

    agent {
        node {
            label 'master'
        }
    }

    tools { 
        maven 'maven' 
    }

    options {
        buildDiscarder logRotator( 
                    daysToKeepStr: '15', 
                    numToKeepStr: '10'
            )
    }

    environment {
        APP_NAME = "STUDENT_APP"
        APP_ENV  = "DEV"
    }

    stages {
    	stage('Stage 1 - 21049462') {
        	steps {
            	sh 'echo "Stage 1 Completed - 21049462"'
            }
        }

        stage('Stage 2 - 21049462') {
        	parallel {
	        	agent {
	        		docker {
	        			image 'apache2-21049462-image'
	        			args '-d'
	        		}
	        	}
	        	steps {
	        		sh 'echo "Stage 2 Completed - 21049462"'
	        	}
	        	stage('Stage 3 - 21049462') {
	        		steps {
	        			sh 'echo "Stage 3 Completed - 21049462"'
	        		}
	        	}
        	}
        }
        
        	
        	
        

        stage('Stage 4 - 21049462') {
        	steps {
        		input("Proceed to release the work?")
        	}
        }
        stage('Stage 5 - 21049462') {
        	when {
        		sh 'echo "Work Released - 21049462"'
            }       
        }

    }   
}
