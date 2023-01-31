pipeline{
    agent any
    stage('Docker Build'){
            steps{
                sh "docker build -t angular-test-docker:latest ."
            }
    }
    stage('Launch Application') {
            steps {
                sh "docker run --rm -itd -p 4200:80 --name docker-angular-app angular-test-docker:latest"
              
            }
    }
}
