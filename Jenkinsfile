pipeline{
    agent any
    environment{
        SONAR = tool 'qube'
    }
    stages{
        stage('git'){
            steps{
                
            echo "Iam Checking out"
            }
            
        }
        stage('test'){
            steps{
                
            withSonarQubeEnv(credentialsId: 'Jenkins') {
sh " $SONAR/bin/sonar-scanner -Dsonar.projectName=Bank -Dsonar.projectKey=Bank"
                
}
            }
        }
    }
}
