pipeline{
    agent any
 environment {
 docker_hub_credentials=credentials('DockerHubCred') 
                      
 } 
    stages{
    
stage('Using Credentials as environment variable'){
    steps {
       echo "${docker_hub_credentials_USR} ,${docker_hub_credentials_PSW}"
     }

    }
   //  stage('Making Credentials this stage specific') {
   //    steps   {
   //     withCredentials([usernamePassword(credentials:'DockerHubCred',
   //                     usernameVariable:USER, passwordVariable:PWD)]){
   //           sh  " echo ${USER},${PWD} "

   //        }      
   //    }
   // }
    }
}
