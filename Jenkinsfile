pipeline {
        agent any
        environment {
	DOCKERHUB_CREDENTIALS=credentials('DockerHub')
	DOCKERHUB_CREDENTIALS=credentials('dockerhub2')	
	}

    
        stages {
       //    stage('pull') {
       //         steps {
        //           docker.withRegistry('https://registry.hub.docker.com', 'DockerHub')
         //          sh 'docker pull srilekhas/php:latest'
           //     }
           // } 
            
            stage('tag image') {
                steps {
                    sh 'docker tag srilekhas/php:latest 9492261286/php-new:latest'
		    // DOCKERHUB_CREDENTIALS=credentials('dockerhub2')	
                }
            }
            stage('push image') {
                steps {
		    // docker.withRegistry('https://registry.hub.docker.com', 'dockerhub2')	
                    // sh 'docker login -u 9492261286 -p Lekha1998'
                    sh 'docker push 9492261286/php-new:latest'
                }
            }
        } 
}	
