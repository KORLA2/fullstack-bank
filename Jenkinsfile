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

//                 withCredentials([string(credentialsId: 'sonartoken', variable: '')]) {
//    sh " $SONAR/bin/sonar-scanner -Dsonar.projectName=Bank -Dsonar.projectKey=Bank"
// }
//             withSonarQubeEnv('QubeSOnar') {
//  sh " $SONAR/bin/sonar-scanner -Dsonar.projectName=Bank -Dsonar.projectKey=Bank"
                
// }
                echo "Iam running sonar tests"
            }
        }
stage('build and push'){
    steps{
        
    docker build -t backend app .
}
}
    }
}
