node{

    stage('SCM Checkout')
    {
        git credentialsId: '4cc785e9-441d-4818-a248-2bfb2148004d', url: 'https://github.com/VardhanNS/phpmysql-app.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'sudo docker-compose build'
        sh 'sudo docker-compose up -d'
    }
  stage('PUSH image to Docker Hub')
    {
          
             sh 'sudo docker login -u "rockysam619" -p "iknewit2@" docker.io'
             sh 'sudo docker push rockysam619/onlineshop1_web'
 
    }
}
