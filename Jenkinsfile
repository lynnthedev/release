pipeline {
	agent none
    tools { 
        maven 'maven'
    }

    stages {
    	stage('Stage 1 - 21049462') {
        	steps {
            	sh 'echo "Stage 1 Completed - 21049462"'
            }
        }

        stage('Parallel') {
        	parallel {
        		stage('Stage 2 - 21049462') {
        			agent {
        				
        				reuseNode true
        				docker {
	    					image 'apache2-21049462-image'
	    					args '-d'
	    					label "docker-create"
	    				}
        			}
        			steps {
        				sh 'echo "Stage 2 Completed - 21049462"'
					}
    				
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
        		Proceed
        		sh 'echo "Work Released - 21049462"'
            }       
        }

    }   
}
