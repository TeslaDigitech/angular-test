pipeline{
    agent any
  
  stages {  
  stage('Docker Build'){
      
            steps{
                sh "docker build -t angular-test-docker:latest ."
            }
      
    }
    stage('Stop Running Container ') {
            steps {
                sh "docker stop docker-angular-app || true" 
              
            }
        } 
  
    stage('Launch Application') {
      
            steps {
                sh "docker run --rm -itd -p 4200:80 --name docker-angular-app angular-test-docker:latest"
            }
      
    }
    stage('Prune unused docker images') {
            steps {
                sh "docker image prune -f" 
              
            }
        } 
  
}
}
