pipeline{
    agent any
  
  stages {  
  stage('Docker Build'){
      
            steps{
                sh "sudo docker build -t angular-test-docker:latest ."
            }
      
    }
  
    stage('Launch Application') {
      
            steps {
                sh "sudo docker run --rm -itd -p 4200:80 --name docker-angular-app angular-test-docker:latest"
            }
      
    }
}
}
