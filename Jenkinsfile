pipeline{
    agent any
    environment{
        
        SONAR = tool 'sonarscanner'
    }
   
    stages{
        stage('git'){
            steps{
                
            echo "Iam Checking out"
            }
            
        }
        stage('test'){
            steps{

                withCredentials([string(credentialsId: 'sonartoken', variable: '')]) {
   sh " $SONAR/bin/sonar-scanner -Dsonar.projectName=Bank -Dsonar.projectKey=Bank"
}
//             withSonarQubeEnv('sonarqube') {

                
// }
            }
        }
    }
}
