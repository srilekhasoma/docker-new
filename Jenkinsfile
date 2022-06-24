node {
    checkout scm
    stage ('Pull image') {
    docker.withRegistry('https://registry.hub.docker.com', 'DockerHub') {
    sh 'docker pull srilekhas/php:latest'
    }  
    }
}
    stage ('tag image to private-registry-2') {
    sh 'docker tag srilekhas/php:latest 9492261286/php-new:latest'
    // image = docker.image('9492261286/php-new:latest') 
    }  
