pipeline {    
    agent any
    
   // environment{
//         IMAGE_REPO_NAME="authorization_service"
//         IMAGE_TAG="practice"
//         REPOSITORY_URI = ("jenkins secret"
//         AWS_ACCESS_KEY_ID=("jenkins secret")
//         AWS_SECRET_ACCESS_KEY=('jenkins secret')
  //  }
        
    stages {
        
        stage('Cloning Git') {
            steps {
               checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Asuradipati/static-html-docker-server.git']]])
                //  checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/cheboluvenkatesh/static-html-docker-server.git']]])
                //checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/AkurathiHarshitha/static-html-docker-server.git']]])
            }
        }
        
        
      //  stage('build'){
       //   steps{
        //     sh'''
        //      npm install
       //        npm run build
       //         '''
       //     }
     //   }
   // Building Docker images
//     stage('Building image') {
//      steps{
//        script {
//            dockerImage = docker.build "${IMAGE_REPO_NAME}:${IMAGE_TAG}"
//         }
//       }
//     }
   
  //  Uploading Docker images into AWS ECR
//     stage('Logging into AWS ECR') {
//            steps {
//                 script {
//                     sh "AWS_ACCESS_KEY_ID=${AWS_ACCESS_KEY_ID} AWS_SECRET_ACCESS_KEY=${AWS_SECRET_ACCESS_KEY} aws ecr get-login-password --region ${AWS_DEFAULT_REGION} | docker login --username AWS --password-stdin ${AWS_ACCOUNT_ID}.dkr.ecr.${AWS_DEFAULT_REGION}.amazonaws.com"
//                 }
                 
//             }
//         }
        
       stage('Pushing to ECR') {
             steps{  
                 script {
                       sh "echo hello"
//                     sh "docker tag ${IMAGE_REPO_NAME}:${IMAGE_TAG} ${REPOSITORY_URI}:$IMAGE_TAG"
//                     sh "docker push ${AWS_ACCOUNT_ID}.dkr.ecr.${AWS_DEFAULT_REGION}.amazonaws.com/${IMAGE_REPO_NAME}:${IMAGE_TAG}"
//                     sh "docker images -q ${IMAGE_REPO_NAME}:${IMAGE_TAG} | xargs docker rmi -f"
                }
             }
        }
   
    }
}


