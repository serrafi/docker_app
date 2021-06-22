node {
    def docker_app
    stage('checkout git rep') { // for display purposes
        git credentialsId: 'ibraboy', url: 'https://github.com/serrafi/docker_app'
        
    }
    stage('docker Build image ') {
        sh 'docker build -t ibrahimserrafi/img1:latest identidock/.'
        
        
    }
    stage('push to docker') {
    withCredentials([usernameColonPassword(credentialsId: 'dockerp', variable: 'dockerhubt')]) {
         sh "docker login -u ibrahimserrafi -p Ibrahim2015@1 docker.io"
      }
    sh 'docker push ibrahimserrafi/img1:latest'
    }
    stage('run container') {
        sh 'docker run -t -d  --name testp ibrahimserrafi/img1:latest'
    }
    
}
