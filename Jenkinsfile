#! groovy
node {
    stage('code') {
        
        sh " git branch: 'main', url: 'https://github.com/cvsuneel/offers-microservice-spring-boot.git' "
    }
    stage('Build') {
        sh 'docker build -t offers .'
    }
    stage('Deploy') {
        sh 'docker run -d -p 1001:1001 --restart unless-stopped --name offers offers'
    }
}
