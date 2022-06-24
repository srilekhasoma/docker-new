pipeline {
        agent any
    
        stages {
            stage('pull') {
                steps {
                    sh 'echo "$Lekha1998" | docker login --username srilekhas --password-stdin'
                    sh 'docker pull srilekhas/php:latest'
                }
            }
            
            stage('tag image') {
                steps {
                    sh 'docker tag srilekhas/php:latest 9492261286/php-new:latest'
                }
            }
            stage('push image') {
                steps {
                    sh 'docker login -u 9492261286 -p Lekha1998'
                    sh 'docker push 9492261286/php-new:latest'
                }
            }
        }
    }  
