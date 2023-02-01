pipeline{
    agent any
  
  stages {  
  stage('Docker Build'){
      
            steps{
                sh "docker build -u 0 -t angular-test-docker:latest ."
            }
      
    }
  
    stage('Launch Application') {
      
            steps {
                sh "sudo docker run --rm -itd -u 0 -p 4200:80 --name docker-angular-app angular-test-docker:latest"
            }
      
    }
}
}
