pipeline{
    agent any
    // environment{
    //     SONAR = tool 'qube'
    // }
    tool{
        SONAR = 'qube'
    }
    stages{
        stage('git'){
            steps{
                
            echo "Iam Checking out"
            }
            
        }
        stage('test'){
            steps{
                
            withSonarQubeEnv('sonarqube') {
sh " $SONAR/bin/sonar-scanner -Dsonar.projectName=Bank -Dsonar.projectKey=Bank"
                
}
            }
        }
    }
}
