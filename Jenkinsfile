pipeline{
    agent any
    environment{
        
        SONAR = tool 'sonarscanner'
    }
   tools{
       Docker 'Docker'
   }
    stages{
        stage('git'){
            steps{
                
            echo "Iam Checking out"
            }
            
        }
        stage('test'){
            steps{

//                 withCredentials([string(credentialsId: 'sonartoken', variable: '')]) {
//    sh " $SONAR/bin/sonar-scanner -Dsonar.projectName=Bank -Dsonar.projectKey=Bank"
// }
            withSonarQubeEnv('QubeSOnar') {
 sh " $SONAR/bin/sonar-scanner -Dsonar.projectName=Bank -Dsonar.projectKey=Bank"
                
}
            }
        }
stage('build and push'){

    sh "docker-compose up -d "
}
        
    }
}
